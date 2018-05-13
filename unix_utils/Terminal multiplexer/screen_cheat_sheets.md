 <deatils>
<details>
 <summary>link</summary>
 https://www.gnu.org/software/screen/manual/screen.html
 </details>
 </details>
 
 Hotkeys
============================
    remeber
    pr = prefix def "ctrl+a"
    C-z = ctrl + z
    ----------------------------

    "pr + A"                                  -   rename window
    "pr + C-a"                                -   witch to previous window
    "pr + c" or "pr + C-c"                    -   create new window
    "pr + d" or "pr + C-d"                    -   deatach session
    "pr + I"                                  -   enable output loging
    "pr + f" or "pr + C-f"                    -   flow / deflow
    "pr + C-g"                                -   toggle visual bell
    "pr + h"                                  -   Write a hardcopy of the current window to the file “hardcopy.n”
    "pr + H"                                  -   Toggle logging of the current window to the file “screenlog.n”.
    "pr + k" or "pr + K" or "pr + C-k"        -   kill current the window
    "pr + l" or "pr + C-l"                    -   redraw current window
    "pr + L"                                  -   Tell screen to turn on automatic output logging for the windows. 
    "pr + m" or "pr + C-m"                    -   show previous monitoring window message
    "pr + M"                                  -   activate monitoring in the current window
    "pr + n" or "pr + C-n" or "pr + SPACE"    -   select next window
    "pr + N"                                  -   show number and title of the current window
    "pr + q" or "pr + C-q"                    -   Command: xon
    "pr + O"                                  -   disable logging otput
    "pr + p" or "pr + C-p" or "pr + BACSPACE" -   select previous window
    "pr + r" ot "pr + C-r"                    -   wrap on / wrap off 
    "pr + s" or "pr + C-s"                    -   Command: xoff
    "pr + t" or "pr + C-t"                    -   Show current time
    "pr + v"                                  -   show version screen
    "pr + V"                                  -   mode: enter gigraph
    "pr + w" or "pr + C-w"                    -   Show all windows in current session
    "pr + x" or "pr + C-x"                    -   lock session    
    "pr + C-z" or "pr + z"                    -   Sleep go to the background. like as in terminal enter ctrl+z (fg - foreground, bg - background)

    
     "pr + ?"                                  -  help
     "pr + C-\"                                -  kill all windows and terminate screen
     "pr + ""                                  -  List windows in current session    
     
     "pr + Num 0,1,2.."                        -  select window 0,1,2....9
     
     "pr + {" or "pr + }"                      -  copy and paste previous command line
     "pr + _"                                  -  Start/stop monitoring the current window for inactivity
     "pr + *"                                  -  Show the listing of attached displays
     
###### buffer   
     "pr + >"                                  -  Write the paste buffer out to the screen-exchange file
     "pr + <"                                  -  Read the screen-exchange file into the paste buffer
     "pr + ="                                  -  Delete the screen-exchange 

##### managing split (separated) windows     

     "pr + F"           -  resize region
     "pr + Q"           -  Delete all regions but the current one                           -     
     "pr + X"           -  Kill current region
     "pr + z"           -  zoom current separated window (invisible other separated window)  
     "pr + |"           -  split (separate) vertically (top/bottom)
     "pr + S"           -  split (separate) horizontally (left/right)
     "pr + TAB"         -  switch next region (separated window)
     
    

     
##### COPY MODE
     
     "pr + [" or "pr + C-[" or "pr + ESC"     - activa copy mode
     "pr + ]" or "pr + C-]"                   - pastle in buffer screen
     
###### ------------ inside copy mode

                        Function                vi       
                   Back to indentation     ^             
                   Clear selection         Escape        
                   Copy selection          Enter
                   Copy text in page       C-m
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

    :help                       - help
    :source file                - source file
    :meta                       - send prefix
    :suspend                  - sleep process
    :lastmsg                   - show previous multiplexer message



###### -------------- sessions ---------------------------------------

    :detach                   - detach session

  
 ###### ------------- window -----------------------------------------
 
    :screen                     - create new window    
    :next                       - switch to next window    
    :prev                       - switch to previous window        
    :windows                    - list windows
    :redisplay                  - redraw current window    
    :windowlist -b              - choose window interactively        
    :kill                       - close current window      

###### -------------------- regions ----------------------------------------
    :split                      - split into top and bottom regions
    :focus                      - move down to next regions
    :resize =                   - make regions same height
    :remove                     - kill current region
    :only                       - kill all regions except current regin
    :clear                      - clear current region 
    :log                        - logging region to the file
    :log off                    - turn off logging        
    :resize +n                  - increase size of n           
    :resize -n                  - reduce size of n                       
    :resize n                   - set size n


###### ------------------- copy mode ------------------------------------------- 
    
    :copy                       - enter copy mode        
    :paste                      - paste most recent buffer     
    :writebuf /path             - write buffer to file       
    :radbuf /path               - copy file to buffer         
  


terminal 
==================
    screen -r name -X command                                                      - send screen session name command 
    screen -r name -X stuff "ls $(echo -ne '\015')"                                - run ls in session name
    screen vim /etc/motd                                                           - run vim in new session
    screen -list                                                                   - show tmux current sessions       
    screen -r                                                                      - attach (connect) current session
    screen                                                                         - create new tmux session
    screen -r -t session_pid or session_name                                       - attach neme session      
    screen -r name -X quit                                                         - kill session name      
    screen -list | grep : | cut -d. -f1 | awk '{print substr($1, 0)}' | xargs kill - kill all screen current sessions
   



