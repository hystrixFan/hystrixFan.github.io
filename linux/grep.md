# Grep

## Lines after and before the match
Grep 2 or 3 lines, one containing the searched text, and the others just below or over it
* `grep -A2 SEARCHED_TEXT`	tells grep to include 2 line after the match
* `grep -B1 SEARCHED_TEXT`	tells grep to include 1 line before the match
* `-C`	includes lines both before and after the match

{% include footer.html content=" > [Linux](/linux) > grep " %}