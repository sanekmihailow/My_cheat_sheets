  Навигация
============================
    "*" , "#"                                      -   блочное выделение одного или нескольких слов
    "-"                                            -   перемещение назад по начальному строки (^)
    "+" "Enter"                                    -   перемещение вперед по начальному строки (^)

    "Ctrl + w"  0) "Ctrl +w" or "ctrl + стрекли вправо,влево" - перемещение между окнами
                1) "v"                                        - разделение по вертикали
                2) "s"                                        - разделение по горизонтали
                3) "q"                                        - отмена, закрытие окна (аналог :q)

    "shift + G" , "]]"                             -   перейти на конец строки
    "gg" , "[["                                    -   перейти на начало строки
    "{" , "}"                                      -   пермещаться по абзацам вперед, назад
    "n" , "N"                                      -   поиск
    "gf"                                           -   go to file
    "H" , "M" , "L"                                -   перейти вначло, середину, низ
    "число j"                                      -   перемещает вниз на определенное число строк
    "число G"                                      -   перемещает на начало числа строки
    "число стрелки: влево, вправо, вниз, вверх"    -   перемещает на такое число туда
    "%"                                            -   перейти к парной скобке
    "zFa{" , "zFa(" , "zFa["                       -   скрытие от начала скоб и до конца

    "Ctrl + L"                                     -   перерисовывает экран
    "shift + U"                                    -   перевести в верхний регистр
    "shift + u"                                    -   перевести в нижний регистр

#### ___ Выравнивание
1) Сначала выделяем текст -> затем вводит `:'<,'>normal f:5a ` где `:`-разделитель, `5a`-число дальнейших отступов от разделителя, `пробел`- дальнейшие отступы
2) затем выделяем обсласть до которой хотим сократить
3) далее <kbd>shift + <</kbd> -сокращает на 5 оступов
4) затем повторяем <kbd>.</kbd> -повторяем пока не выравниться
5) оригинал [stack exchange](https://vi.stackexchange.com/questions/594/how-to-left-align-two-columns-of-text/20726)

<a href="https://i.stack.imgur.com/FvLhf.gif"><img src="https://i.stack.imgur.com/FvLhf.gif" width="400" title="Align"/></a>





РАБОТА С ТЕКСТОМ
=======================
    5dd+1= "6dd" 5yy и т.д.                        -  число строк, 5yw - число слов
    "3yw"                                          -  скопировать 3 слова c начала первого слова (пример bitnewstoday.us 1 -bitnewstoday 2-. 3-us)
    "x" , "del", ">"                               -  удалить символ без вставки
    "s"                                            -  заменить символ и вставить один или несколько
    "r" , "R"                                      -  заменить один символ, R - режим insert (пишет повверх остальных)
    "i" , "I"                                      -  начать редактирование с текущего символа, I - с начала строки
    "a" , "A"                                      -  начать редактирование со следующего символа , А - с конца строки
    "e" , "w" , "W"                                -  двигаться вперед по началу и концу символов
    "b" , "B"                                      -  двигаться назад по началу символов
    "ctrl + r"                                     -  отмена отмены(как ctrl +y)
    "u"                                            -  отмена действий(как ctrl +z)
    "o" , "O"                                      -  режим ввода после текущей строки , О - перед текущей строкой
    "p" , "P"                                      -  Вставка после текущей строки , Р -перед
    "cc" , "c"                                     -  вырезать строку и перейти в режим вставки, с - выделенное
    "dd" , "d"                                     -  Вырезать строку ( удалить и оставить в буфере последнюю запись) , d - выделенное
    "dw" , "db"                                    -  удалить слово от текущего положения вперед, назад
    "yw" , "yb"                                    -  скопировать слово от текущего положения вперед, назад
    "cw" , "cb"                                    -  вырезать слово от текущего положения вперед, назад

    "ma"                                           -  метка в регистре "a"
    "'a"                                           -  перейти к метке в регистре "а"
    "yy" , "y"                                     -  копировать строку , у-  выделенное







Регистры
==================
""ayw"                                             -  скопировать в буфер " и регистр "а" слово
""ap"                                              -  вставить из буфера " и регситра "а" слово

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
    ':tabnew путь'                                 -  создать новую вкладку
                   "Ctrl + PgUP" , "Ctrl + PgDN"   -  перемещение между вкладками (вперед , назад)

    ':Q'                                           -  режим ed редактирования
    '/' , '?'                                      -  поиск с начала , конца
    ':e Путь'                                      -  открыть для редактирования файл
    ':r путь or !command'                          -  вставить из фийла или команды текст
    ':sh'                                          -  перейти в shell
    ':Nread ftp://...'                             -  открыть в vim файл на удаленном хосте
    ':%s/ab/db/gi'                                 -  заменить глобально ab на db , i - ignorecase
    ':1,3s/ab/db/'                                 -  заменить ab на db c 1 по 3 строку
    ':%!tr 'A-Z' 'a-z''                            -  изменить регистр букв с маленьких на большой глобально
    ':1,3!tr 'A-Z' 'a-z''                          -  изменить регистр букв с маленьких на большой с 1 по 3 строку
    ':/tag/,/untag/s/abc/def/'                     -  заменяет abd на def между "/tag" и "/untag"
    ':g/^$/d'                                      -  удалить пустые строки
    ':%le' or ':79,97s/^\s*//'                     -  удалить пустые пробелы в начале строки или в определенных строках
    ':s/\s\+$'                                     -  удалить пустые проблелы в конце на текущей строке
    ':%s/\s\+$' or ':%s/\s\+$//'                   -  удалить пустые проблелы в конце на всех стоках в файле
    ':%s/\r\n/\r/'                                 -  удалить виндовый ^M
    ':g/^\(#\|$\)/d' or ':g/\v^(#|$)/d'            -  удалить комментарии
    ':set'                                         -  показать текущие настройки
    ':buffers'                                     -  показать кол-во буфферов
    ':registers'                                   -  показать кол-во регистров
    
    ':sort u'                                      -  отсортировать и убрать дубликаты в строках

    ':set syntax=python'                           -  установить синтаксис Python
    ':set ro'                                      -  сделать только для чтения
    ':set foldmethod=indent'                       -  zr , zt , zc, zO

    ':iab abvr ACCESS bridge version raid'         -  сделать абривиатуру и раскравать ее в тексте
    ':e ++enc=koi8-r'                              -  сделать читаемой в vim кодировку koir8-r

    ':res +/-25'                                   -  перераспределить размер окна 
    ':vertical resize +/-15'                       -  перераспределить размер окна по вертикали


        set syntax=dmesg
        set syntax=syslog
        set syntax=kernel
        set syntax=samba
        set syntax=systemd
        set syntax=messages
        set filetype=messages
        set filetype=dmesg
