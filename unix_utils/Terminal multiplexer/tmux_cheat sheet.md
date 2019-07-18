  Hotkeys
============================
    remeber
    pr = prefix def ("ctrl+b")
    C-z = ctrl + z
    ----------------------------


| ***Action*** | ***hotkey*** |
|---|---|
| Show current time  | <kbd>pr + c</kbd><br>  
| deatach session  | <kbd>pr + d</kbd><br>  
| deatach and select panes  | <kbd>pr + D</kbd><br>  
| find window (search all windows open)  | <kbd>pr + f</kbd><br>  
| view you session . nae window and time . date  | <kbd>pr + i</kbd><br>  
| kill current the window | <kbd>pr + k</kbd><br>  
| kill current the Sessions (Server) | <kbd>pr + K</kbd><br> 
| select previous window  | <kbd>pr + l</kbd><br>  
| select previous Session  | <kbd>pr + L</kbd><br>  
| mark the current window (add M to the end) | <kbd>pr + m</kbd><br>  
| select next window | <kbd>pr + n</kbd><br>  
| select previous window  | <kbd>pr + p</kbd><br>  
| show current pane nubmber | <kbd>pr + q</kbd><br>  
| source tmux conf  | <kbd>pr + r</kbd><br>  
| Restore previous sessions after reboot (tmux resurrect) | <kbd>pr + R</kbd><br>  
| selest list sessions | <kbd>pr + s</kbd><br>  
| Save current sessions after reboot (tmux resurrect) | <kbd>pr + S</kbd><br>  
| Show current time  | <kbd>pr + t</kbd><br>  
| Show list window in current pane  (like as "pr + f") | <kbd>pr + w</kbd><br>  
| Kill current pane | <kbd>pr + x</kbd><br>  
| Sleep go to the background. like as in terminal enter ctrl+z (<b>fg</b> - foreground, <b>bg</b> - background)| <kbd>pr + C-z</kbd><br>
| |
| |
| help  | <kbd>pr + ?</kbd><br>  
| select next sessions | <kbd>pr + )</kbd><br>
| select previous sessions  | <kbd>pr + (</kbd><br>
| rename corrent Session  | <kbd>pr + $</kbd><br>
| kill window (include  all separated)  | <kbd>pr + &</kbd><br>
| rename window | <kbd>pr + ,</kbd><br>
| move current window to  (	. sessname )<br>  ( . sessnum:position ) | <kbd>pr + .</kbd><br>
| |
| PGDOWN  | <kbd>pr + PGDN</kbd><br>
| PGUP  | <kbd>pr + PGUP</kbd><br>
| select window 0,1,2....9  | <kbd>pr + Num 0,1,2..</kbd><br>
        

## managing split (separated) windows     

| ***Action*** | ***hotkey*** |
|---|---|
| switch next pane (separated window) | <kbd>pr + o</kbd><br> 
| show current separated window nubmber | <kbd>pr + q</kbd><br> 
| Kill current separated window | <kbd>pr + x</kbd><br> 
| zoom current separated window (invisible other separated window)  | <kbd>pr + z</kbd><br> 
| split (separate) vertically (top/bottom)  | <kbd>pr + "</kbd><br> 
| split (separate) horizontally (left/right)  | <kbd>pr + %</kbd><br> 
| switch previous separated window | <kbd>pr + ;</kbd><br> 
| move the current pane to the next position | <kbd>pr + }</kbd><br> 
| move the current pane to the previous position    | <kbd>pr + {</kbd><br>
| help  | <kbd>pr + -</kbd><br> 
| help  | <kbd>pr + +</kbd><br> 
| around switch vertically or horizontally | <kbd>pr + SPACE</kbd><br>
| combine (unite) all separated in one other window | <kbd>pr + !</kbd><br> 


     
## COPY MODE

| ***Action*** | ***hotkey*** |
|---|---|
| activa copy mode | <kbd>pr + [</kbd><br>
| pastle in buffer tmux | <kbd>pr + ]</kbd><br>

     
### ------------ inside copy mode

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
    tmux list-commands                                                                          - show tmux commands
    tmux list-session                                                                           - show tmux sessions
    tmux ls                                                                                     - show tmux current sessions       
    tmux attach / tmux a                                                                        - attach (connect) current session
    tmux new                                                                                    - create new tmux session
    tmux a -t session_name                                                                      - attach current session name      
    tmux kill-session -t session_name                                                           - kill session name      
    tmux ls | grep : | cut -d. -f1 | awk '{print substr($1, 0, length($1)-1)}' | xargs kill     - kill all tmux current session         
    tmux kill-server                                                                            - kill all tmux session 
    tmux command -t name                                                                        - send command to session name 
    tmux send-keys -t name 'ls' C-m                                                             - run ls in sessein name
    tmux new-window vi /etc/motd                                                                - run vi in new session  
   



