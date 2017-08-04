# SSL
# Skip SSL certificate verification
```java
import lombok.extern.slf4j.Slf4j;

import javax.net.ssl.*;
import java.security.KeyManagementException;
import java.security.NoSuchAlgorithmException;
import java.security.SecureRandom;
import java.security.cert.CertificateException;
import java.security.cert.X509Certificate;

@Slf4j
public class SSLCertificateCheckingSkipper {
  public static void skipAllVerifications() throws NoSuchAlgorithmException, KeyManagementException {
    final HostnameVerifier allHostsValid = new AllHostnamesVerifier();
    final SSLContext sc = SSLContext.getInstance("SSL");
    sc.init(null,
        new TrustManager[] {new TrustAllCertsManager() },
        new SecureRandom());
    HttpsURLConnection.setDefaultSSLSocketFactory(sc.getSocketFactory());
    HttpsURLConnection.setDefaultHostnameVerifier(allHostsValid);
    log.info("Patched SSLContext / skipping all SSL-Verifications.");
  }

  public static final class AllHostnamesVerifier implements HostnameVerifier {
    @Override
    public boolean verify(String hostname, SSLSession sslSession) {
      return true;
    }
  }

  public static final class TrustAllCertsManager implements X509TrustManager {

    @Override
    public void checkClientTrusted(X509Certificate[] x509Certificates, String s) throws CertificateException {
    }

    @Override
    public void checkServerTrusted(X509Certificate[] x509Certificates, String s) throws CertificateException {
    }

    @Override
    public X509Certificate[] getAcceptedIssuers() {
      return null;
    }
  }
}
```

{% include footer.html content=" > [Java](/java) > ssl " %}
