# Files

## Copy file
`cp fileName dirName`

## Count files in directory
1) `ls -1 | wc -l`
2) `find dirName -type f | wc -l`   
e.g. such in the current dir
`find . -type f | wc -l`

## Count lines in a file
`wc -l fileName`
 
## Split file
1) `split fileName`
2) `split fileName splittedFileNamePrefix_`   
so each part of the splitted file has a prefix "splittedFileNamePrefix_"   
e.g. splittedFileNamePrefix_aa, splittedFileNamePrefix_ab etc. 

The default size for each split file is 1000 lines. `-l` put number lines/records per output file.   
`split fileName splittedFileNamePrefix_ -l 10000`

## Insert and append a lines
### Insert a line before 'N'th line 
`sed -i 'N i\text to be inserted' filePattern` or   
`sed -i 'N i text to be inserted' filePattern`     
In case you wish to append lines in the file and save the changes (i.e. edit the file in place), you will have to use the option `-i`.
  Append/Insert a line
  https://unix.stackexchange.com/questions/99350/how-to-insert-text-before-the-first-line-of-a-file
  

#### Example
Insert text before the first line in a file   
`sed -i '1 i\text to be inserted' filePattern` 
 
### Append a line after 'N'th line 
`sed -i 'N a text to be appended' filePattern`

# Links
## Append/Insert a line
[SED COMMAND IN LINUX - APPEND AND INSERT LINES TO A FILE](http://www.yourownlinux.com/2015/04/sed-command-in-linux-append-and-insert-lines-to-file.html)  

{% include footer.html content=" > [Linux](/linux) > Files " %}

  