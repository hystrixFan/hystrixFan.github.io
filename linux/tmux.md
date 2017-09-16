tmux list-sessions  
tmux a   // atach the last opened session  
tmux a -t sessionName   // atach the session with the name sessionName  
tmux new -s sessionName // create the session with the name sessionName
 
 
Wenn man in in einer Session ist, kann man mit Ctrl-B in den TMUX Befehl-Modus wechseln. Der Modus hält nur bis zum ersten Befehl. Für den nächsten Befehl muss man wieder Ctrl-B eingeben.
 
## Commandozeile
ctrl-B + :
 
ctrl-B
slogin rechnername
 
# Panes
 
ctrl-B und "  ein Window oder Pane horizontal spalten
ctrl-B und %  ein Window oder Pane vertikal spalten
 
## switch to other pane          ctrl-B und o
 
## Synchronieren aller Panes anschalten:
Ctrl-B :setw synchronize-panes
Ctrl-B :setw synchronize-panes on
 
## Synchronieren aller Panes ausschalten:
Ctrl-B :setw synchronize-panes off
 
# Windos
 
## anderes window
Ctrl-B und cc
 
## Bei mehreren Fenstern
n  next  p  previuos   (oder 0..9 für Window-Nummer aus Statuszeile)
 
## maximieren und minimeieren (zoome)
Ctrl-B und z  (maximieren und minimeieren)
 
## Navigation innerhalb des Fensters
ein    Ctrl-B und [  d.h. Ctrl-B und AltGr und die Taste mit 8
raus   Enter