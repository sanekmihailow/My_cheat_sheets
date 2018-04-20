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
    
    
    
    
     "pr + ?"     -   help
     "pr + )"     -   select next sessions
     "pr + ("     -   select previous sessions
     "pr + $"     -   rename corrent Session
     "pr + &"     -   kill window (include  all separated)
     "pr + ,"     -   rename window
     "pr + ."     -   move current window to  (	. sessname )
                                              ( . sessnum:position )
     "pr + PGDN"  -   PGDOWN
     "pr + PGUP"  -   PGUP
     "pr + Num 0,1,2.."   - select window 0,1,2....9

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
=======================
 "pr + :"       -  command mode

------------------ other --------------------------------------

  list-keys                                -         help
source-file file                  source file
send-prefix
suspend-client                    sleep process
show-messages                     show previous multiplexer message



###### -------------- sessions ---------------------------------------

detach-client                     detach session
new                               new session
new -s foo                        new named session
choose-session                    switch session                     

  
 ###### ------------- window -----------------------------------------
 
new-window                        create new window    
next-window                       switch to next window    
previous-window                   switch to previous window    
select-window -t :n               select window n    
list-windows                      list windows
move-window                       move current window to another session
refresh-client                    redraw current window    
choose-window                     choose window interactively        
kill-window                       close current window      

###### -------------------- pane ----------------------------------------
split-window -h                   split into left and right panes        
split-window                      split into top and bottom panes  
select-pane                       switch to next panes      
rotate-window                     rotate panes      
rotate-window -D                  reverse rotate panes          
swap-pane -U                      change place current and previous pane        
swap-pane -D                      clange place current and next pane      
next-layout                       change vertical or horizaontal around        
confirm-before kill-pane          close current pane            
break-pane                        break(unite) current pane into separate window                        
list-panes                        list panes
display-panes                     display pane numbers
clear-history                     clear current pane
pipe-pane "cat > /tmp/tmux.log"   log pane to file         
pipe-pane                         turn off logging
join-pane -s 1                    join window 1 to current window      
join-pane -s 1.0                  join region 0 of window 1 to current window
resize-pane -L n                  resize pane left n cells     
resize-pane -U n                  resize pane up n cells     

###### ------------------- copy mode ------------------------------------------- 
copy-mode                         enter copy mode        
paste-buffer                      paste most recent buffer     
list-buffers                      list buffers     
choose-buffer                     choose buffer to paste interactively 
save-buffer /path                 write buffer to file       
load-buffer /path                 copy file to buffer         
  




Регистры
==================
""ayw" - скопировать в буфер " и регистр "а" слово
""ap" - вставить из буфера " и регситра "а" слово

#####                             Копировать из vima себе

""+yy" или ""*yy"



##### Если по ssh то
    /etc/ssh/sshd_config
           ForwardX11 yes

    ssh -XY user@remote_host -pport
              # deb / ubuntu
    apt install vim-gtk xorg openbox
    и можно еще
    sudo apt-get install xauth
              # arch
    pacman -S gvim
    




Режим ввода команд
=======
    ':tabnew путь' - создать новую вкладку
                    "Ctrl + PgUP" , "Ctrl + PgDN" - перемещение между вкладками (вперед , назад)

    ':Q' - режим ed редактирования
    '/' , '?' - поиск с начала , конца
    ':e Путь' - открыть для редактирования файл
    ':r путь or !command' - вставить из фийла или команды текст
    ':sh'  - перейти в shell
    ':Nread ftp://...' -  открыть в vim файл на удаленном хосте
    ':%s/ab/db/gi' - заменить глобально ab на db , i - ignorecase
    ':1,3s/ab/db/' - заменить ab на db c 1 по 3 строку
    ':%!tr 'A-Z' 'a-z'' - изменить регистр букв с маленьких на большой глобально
    ':1,3!tr 'A-Z' 'a-z'' -  изменить регистр букв с маленьких на большой с 1 по 3 строку
    ':/tag/,/untag/s/abc/def/' - заменяет abd на def между "/tag" и "/untag"

    ':set'  - показать текущие настройки
    ':buffers' - показать кол-во буфферов
    ':registers' - показать кол-во регистров

    ':set syntax=python' - установить синтаксис Python
    ':set ro' - сделать только для чтения
    ':set foldmethod=indent'  zr , zt , zc, zO

    ':iab abvr ACCESS bridge version raid' - сделать абривиатуру и раскравать ее в тексте





