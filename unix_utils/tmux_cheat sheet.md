  Hotkeys
============================
    remeber
    prefix def (pr) = "ctrl+b"
    C-z = ctrl + z
    ----------------------------

    "pr + c"    -   create new window
    "pr + d"    -   deatach session
    "pr + D"    -   deatach and select panes
    "pr + f"    -   find window (search all windows open)
    "pr + i"    -   view you session . nae window and time . date
    "pr + k"    -   kill current the window
    "pr + K"    -   kill current the Sessions (Server)
    "pr + l"    -   select previous window
    "pr + L"    -   select previous Session
    "pr + m"    -   mark the current window (add M to the end)
    "pr + n"    -   select next window
    "pr + p"    -   select previous window
    "pr + q"    -   show current pane nubmber
    "pr + r"    -   source tmux conf
    "pr + R"    -   Restore previous sessions after reboot (tmux resurrect)
    "pr + s"    -   selest list sessions 
    "pr + S"    -   Save current sessions after reboot (tmux resurrect)
    "pr + t"    -   Show current time
    "pr + w"    -   Show list window in current pane  (like as "pr + f")
    "pr + x"    -   Kill current pane
    "pr + C-z"  -   Sleep go to the background. like as in terminal enter ctrl+z (fg - foreground, bg - background)
    
    
    
    
     "pr + ?"             -   help
     "pr + )"             -   select next sessions
     "pr + ("             -   select previous sessions
     "pr + $"             -   rename corrent Session
     "pr + &"             -   kill window (include  all separated)
     "pr + ,"             -   rename window
     "pr + ."             -   move current window to  (	. sessname )
                                                      ( . sessnum:position )
     "pr + PGDN"          -   PGDOWN
     "pr + PGUP"          -   PGUP
     "pr + Num 0,1,2.."   -   select window 0,1,2....9

##### managing split (separated) windows     

     "pr + o"     -   switch next pane (separated window)
     "pr + q"     -   show current separated window nubmber     
     "pr + x"     -   Kill current separated window
     "pr + z"     -   zoom current separated window (invisible other separated window)  
     "pr + ""     -  split (separate) vertically (top/bottom)
     "pr + %"     -  split (separate) horizontally (left/right)
     "pr + ;"     -  switch previous separated window
     "pr + }"     -  move the current pane to the next position
     "pr + {"     -  move the current pane to the previous position    
     "pr + -"
     "pr + +"     
     "pr + space" -  around switch vertically or horizontally
     "pr + !"     -  combine (unite) all separated in one other window
     
     
##### COPY MODE
     
     "pr + ["     - activa copy mode
     "pr + ]"     - pastle in buffer tmux
     
###### ------------ inside copy mode

                        Function                vi       
                   Back to indentation     ^             
                   Clear selection         Escape        
                   Copy selection          Enter         
                   Cursor down             j             
                   Cursor left             h             
                   Cursor right            l             
                   Cursor to bottom line   L
                   Cursor to middle line   M             
                   Cursor to top line      H             
                   Cursor up               k             
                   Delete entire line      d             
                   Delete to end of line   D             
                   End of line             $             
                   Goto line               :             
                   Half page down          C-d           
                   Half page up            C-u           
                   Next page               C-f           
                   Next word               w             
                   Paste buffer            p             
                   Previous page           C-b           
                   Previous word           b             
                   Quit mode               q             
                   Scroll down             C-Down or J   
                   Scroll up               C-Up or K     
                   Search again            n             
                   Search backward         ?              
                   Search forward          /             
                   Start of line           0             
                   Start selection         Space          


command mode
============================

     
 ##### "pr + :"       -  command mode

------------------ 

    :list-keys                       - help
    :source-file file                - source file
    :send-prefix
    :suspend-client                  - sleep process
    :show-messages                   - show previous multiplexer message



###### -------------- sessions ---------------------------------------

    :detach-client                   - detach session
    :new                             - new session
    :new -s foo                      - new named session
    :choose-session                  - switch session                     

  
 ###### ------------- window -----------------------------------------
 
    :new-window                      - create new window    
    :next-window                     - switch to next window    
    :previous-window                 - switch to previous window    
    :select-window -t :n             - select window n    
    :list-windows                    - list windows
    :move-window                     - move current window to another session
    :refresh-client                  - redraw current window    
    :choose-window                   - choose window interactively        
    :kill-window                     - close current window      

###### -------------------- pane ----------------------------------------
    :split-window -h                 - split into left and right panes        
    :split-window                    - split into top and bottom panes  
    :select-pane                     - switch to next panes      
    :rotate-window                   - rotate panes      
    :rotate-window -D                - reverse rotate panes          
    :swap-pane -U                    - change place current and previous pane        
    :swap-pane -D                    - clange place current and next pane      
    :next-layout                     - change vertical or horizaontal around        
    :confirm-before kill-pane        - close current pane            
    :break-pane                      - break(unite) current pane into separate window                        
    :list-panes                      - list panes
    :display-panes                   - display pane numbers
    :clear-history                   - clear current pane
    :pipe-pane "cat > /tmp/tmux.log" - log pane to file         
    :pipe-pane                       - turn off logging
    :join-pane -s 1                  - join window 1 to current window      
    :join-pane -s 1.0                - join region 0 of window 1 to current window
    :resize-pane -L n                - resize pane left n cells     
    :resize-pane -U n                - resize pane up n cells     

###### ------------------- copy mode ------------------------------------------- 
    :copy-mode                       - enter copy mode        
    :paste-buffer                    - paste most recent buffer     
    :list-buffers                    - list buffers     
    :choose-buffer                   - choose buffer to paste interactively 
    :save-buffer /path               - write buffer to file       
    :load-buffer /path               - copy file to buffer         
  



terminal 
==================
    tmux list-commands                         -  show tmux commands
    tmux ls                                    -  show tmux current sessions       
    tmux attach / tmux a                      -   attach (connect) current session
    tmux new                                   -  create new tmux session
    tmux a -t session_name                     -  attach current session name      
    tmux kill-session -t session_name          -  kill session name      
    tmux ls | grep : | cut -d. -f1 | awk '{print substr($1, 0, length($1)-1)}' | xargs kill     - kill all tmux current session         
    tmux kill-server                           -  kill all tmux session 
   



