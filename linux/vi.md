# vi Editor
{% include simplebreadcrumb.md content=" > [Linux](/linux)> vi " %}
Open file `vi filename`  
  
## Modes
vi has two modes command and insert mode.

1. Insert mode (insert) `i`
2. Command mode `[Esc] key`


## Undo
* `u`	undo

## Insert Text (command mode)
* `i`	insert text before cursor, until [Esc] hit
* `a`	append text after cursor, until [Esc] hit
* `o`	open and put text in a new line below current line, until [Esc] hit
* `O`	open and put text in a new line above current line, until [Esc] hit


## Delete Text (command mode)
* `x`  delete current char
* `nx`  nx delete n chars (right from cursor) 
* `nX`  nX delete n chars (left from cursor) 
* `dd`  delete current line
* `ndd`  delete n line(s)
* `D`  bis Ende der Zeile löschen 

## Cut and Past Text
* `yy`	copy (yank, cut) the current line into the buffer
* `Nyy` or yNy	copy (yank, cut) the next N lines, including the current line, into the buffer
* `p`	put (paste) the line(s) in the buffer into the text after the current line


# Links
[Basic vi Commands](https://www.cs.colostate.edu/helpdocs/vi.html)  
[vi-crashkurs-fur-einsteiger](http://netz10.de/2009/04/28/vi-crashkurs-fur-einsteiger/)