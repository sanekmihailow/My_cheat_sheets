midnight commander hotkeys
==========

remember 

meta = (ESC or ALT)

C-z = (ctl + z)     

### panel


     "meta + i"                         - move to directory from inactual panel on actual panel 
                                             example: actual = (/var/www), inactual ( /usr/local) -> inactual will (/var/www)
     "meta + o"                         - shows contents directory from actual panel on inactual panel
     "meta + t"                         - change view poroperties
     "meta + ,"                         - show panel vertial / horizontal
     "C-l"                              - redraw screen
     "C-r"                              - reread contents in directory
     "C-o"                              - switch to command line
     "C-x, a"                           - show list actual virtual connect
     "C-x, j"                           - show list background procces
     "C-u"                              - to change places panel
     
     
 ### manage
 
      "insert" or "shift + arrow (down/up)" or "shift + t"       - select file, fioled
      "+"                                                        - select files based on a pattern
      "-" or "\"                                                 - unselect files based on a pattern
      "*"                                                        - select all files on this folder
      "meta + shift + H"                                         - show history previous path
      "meta + ."                                                 - show on / show off hidden files (.*)
      "meta + a" or "C-x, p"                                     - paste in shell current path (activity panel)
      "meta + c"                                                 - change current path
      "meta + g" or "HOME"                                       - move top
      "meta + j" or "END"                                        - move down
      "meta + r"                                                 - select middle
      "meta + shift + ?"                                         - advanced search 
      "meta + y"                                                 - move to the previous directory in history
      "meta + u"                                                 - move to the next directory in history
      
      "C-\"                                                      - show stars path
      "C-space"                                                  - show size current selected folder / file
      "C-s"                                                      - fast search
      "C-x, i"                                                   - show fast info of current object
      "C-x. l"                                                   - create hard link
      "C-x, o"                                                   - edit owner and group of current object
      "C-x, q"                                                   - show fast content of file on inactual panel
      "C-x, s"                                                   - create symlink
      "C-x, C-s"                                                 - edit symlink
      
      "shfit + F4"                                               - create new file
      
### shell

     "meta + ENTER"                                 - copy the currently selected file’s name to the shell
     "meta + a" or "C-x, p"                         - copy all current path to the shell
     "meta + h"                                     - show history previous commands
     "meta + shift + A" or "C-x, C-p"               - copy all inactual path to the shell
     
     
      
# tmux vs. screen commands
---

| **Action** | **hotkey** |
|---|---|
| create new file | <kbd>shift + F4</kbd><br>	| <kbd>screen</kbd> | 
