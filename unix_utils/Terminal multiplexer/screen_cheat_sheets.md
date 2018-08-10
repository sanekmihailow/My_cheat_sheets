 <deatils>
<details>
 <summary>link</summary>
 https://www.gnu.org/software/screen/manual/screen.html
 </details>
 </details>
 
 
     remeber
    pr = prefix def "ctrl+a"
    C-z = ctrl + z
    ----------------------------
 
 
 Hotkeys
============================


| ***Action*** | ***hotkey*** |
|---|---|
| rename window | <kbd>pr + A</kbd><br>
| witch to previous window | <kbd>pr + C-a</kbd><br>
| create new window | <kbd>pr + c</kbd> or<br><kbd>pr + C-c</kbd><br> 
| deatach session | <kbd>pr + d</kbd> or<br><kbd>pr + C-d</kbd><br>
| enable output loging | <kbd>pr + I</kbd><br>
| flow / deflow | <kbd>pr + f</kbd> or <br><kbd>pr + C-f</kbd><br>
| toggle visual bell | <kbd>pr + C-g</kbd><br>
| Write a hardcopy of the current window to the file “hardcopy.n” | <kbd>pr + h</kbd><br>
| Toggle logging of the current window to the file “screenlog.n” | <kbd>pr + H</kbd><br>
| kill current the window | <kbd>pr + k</kbd> or<br><kbd>pr + K</kbd> or<br><kbd>pr + C-k</kbd><br>
| redraw current window | <kbd>pr + l</kbd> or<br><kbd>pr + C-l</kbd><br>
| Tell screen to turn on automatic output logging for the windows | <kbd>pr + L</kbd><br> 
| show previous monitoring window message | <kbd>pr + m</kbd><br> or<br><kbd>pr + C-m</kbd><br>
| activate monitoring in the current window | <kbd>pr + M</kbd><br>
| select next window | <kbd>pr + n</kbd><br> or<br><kbd>pr + C-n</kbd> or<br><kbd>pr + SPACE</kbd><br>
| show number and title of the current window | <kbd>pr + N</kbd><br>
| Command: xon | <kbd>pr + q</kbd> or<br><kbd>pr + C-q</kbd><br>
| disable logging otput | <kbd>pr + O</kbd><br>
| select previous window | <kbd>pr + p</kbd> or<br><kbd>pr + C-p</kbd> or<br><kbd>pr + BACKSPACE</kbd><br>
| wrap on / wrap off | <kbd>pr + r</kbd> or<br><kbd>pr + C-r</kbd><br>
| Command: xoff | <kbd>pr + s</kbd> or<br><kbd>pr + C-s</kbd><br>
| Show current time | <kbd>pr + t</kbd> or<br><kbd>pr + C-t</kbd><br>
| show version screen| <kbd>pr + v</kbd><br>
| mode: enter gigraph | <kbd>pr + V</kbd><br>
| Show all windows in current session | <kbd>pr + w</kbd> or<br><kbd>pr + C-w</kbd><br>
| lock session   | <kbd>pr + x</kbd> or<br><kbd>pr + C-x</kbd><br>
| Sleep go to the background. like as in terminal enter ctrl+z <br> (<b>fg</b> - foreground, <b>bg</b> - background) | <kbd>pr + z</kbd> or<br><kbd>pr + C-z</kbd><br>
| | 
| |
| help | <kbd>pr + ?</kbd><br>
| kill all windows and terminate screen | <kbd>pr + C-\\</kbd><br>
| List windows in current session  | <kbd>pr + "</kbd><br>
| |
| select window 0,1,2....9| <kbd>pr + NUM 0,1,2,...</kbd><br>
| |
| copy and paste previous command line  | <kbd>pr + {</kbd> or<br><kbd>pr + }</kbd><br>
| start/stop monitoring the current window for inactivity | <kbd>pr + <b><i>+</i></b></kbd><br>
| Show the listing of attached displays | <kbd>pr + *</kbd><br>

## buffer   

| ***Action*** | ***hotkey*** |
|---|---|
| Write the paste buffer out to the screen-exchange file | <kbd>pr + ></kbd><br>
| Read the screen-exchange file into the paste buffer | <kbd>pr + <</kbd><br>
| Delete the screen-exchange  | <kbd>pr + =</kbd><br>                         -  

## managing split (separated) windows     

| ***Action*** | ***hotkey*** |
|---|---|
| resize region  | <kbd>pr + F</kbd><br>  
| Delete all regions but the current one  | <kbd>pr + Q</kbd><br>  
| Kill current region  | <kbd>pr + X</kbd><br>  
| zoom current separated window (invisible other separated window)  | <kbd>pr + z</kbd><br>  
| split (separate) vertically (top/bottom)  | <kbd>pr + |</kbd><br>  
| split (separate) horizontally (left/right)  | <kbd>pr + S</kbd><br>  
| switch next region (separated window)  | <kbd>pr + TAB</kbd><br>  


     
## COPY MODE

| ***Action*** | ***hotkey*** |
|---|---|
| activa copy mode| <kbd>pr + [</kbd> or<br><kbd>pr + C-[</kbd> or<br><kbd>pr + C-ESC</kbd> or<br><kbd>pr + ESC</kbd><br>
| pastle in buffer screen | <kbd>pr + ]</kbd> or<br><kbd>pr + C-]</kbd><br>

     
### ------------ inside copy mode

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
   



