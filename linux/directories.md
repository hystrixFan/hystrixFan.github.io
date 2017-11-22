# Directories

## List

### List files and directories  
`ls -l folder_pattern`

#### Example
Command  
`ls -l server60*p/application/logs/2017*.log`

### List only directories which names contain the string 'partOfDirectoryName'   
`ls -ld *partOfDirectoryName*`

Result  
```
server601p/application/logs/2017-06-06-0.log
server601p/application/logs/2017-06-06-1.log
server601p/application/logs/2017-06-06-2.log
server602p/application/logs/2017-06-06-0.log
server602p/application/logs/2017-06-06-1.log
server602p/application/logs/2017-06-06-2.log
```

### List with for loop
The same result can be achived with the `for` loop

## Remove full directory
rm -r dirName

{% include footer.html content=" > [Linux](/linux) > Directories " %}