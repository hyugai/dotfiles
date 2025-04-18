NEOVIM'S SETTING-UP FOR PYTHON IN UBUNTU 24.04 (WSL2)

SOME NOTES
- I'm using the default terminal in Windows 11 24H2
- There are some packages in "requirements.txt" file you should install for some purposes as I commented in there 
- To use virtual environments (e.g Anaconda, Miniconda), you should activate it first

KEYBINDINGS (OR "SHORTCUTS")
EDITING
- :e path/to/file -> open and edit the new file in the buffer
- i -> insert or edit the file at the last cursor location
- v -> visual mode or selecting multiple lines
    + v\<number\>'>' -> indent <\number\> times  

MOVING AROUNT WITH THE CURSOR
- 0 -> move to the beginning of the line
- $ -> move to the end of the line
- G -> move to the end of the file
     + \<number\>G -> move the line \<number\> of the file
- gg -> move the first line of the file
- j -> move downward 1 time
    + \<number\>j -> move downward \<number\> times
- k -> move upward 1 time 
    + \<number\>k -> move upward \<number\> times 
- w -> move 1 word forward
    + \<number\>w -> move \<number\> words forward 
- b -> move 1 word backward
    + \<number\>b -> move \<number\> words backward
- f\<character\> -> move to the first found characater in the current line, using ';'-semicolon to move the next found character
    + \<number\>f\<character\> -> move to the \<number\> found character in the current line
- /\<pattern\> -> found substring that match the patter at any line in the file, using character 'n' to move to the next found pattern
- Ctrl + o -> go to the last cursor's position

KILLING
- dd -> delete the current line and store it in buffer ( copy the deleted line(s))
    + d\<number\>G -> delete the current line to line \<number\>
    + dG -> delete the current line to the end of the file
    + df\<character\> -> delete from the current location of the cursor to the first specified character
    + d\<number\>j -> delete the current line and the next \<number\> lines below
    + d\<number\>k -> delete the current line and the next \<number\> lines above 

YANKING
- yy -> copy the current line and store it in buffer ( copy the deleted line(s))
    + y\<number\>G -> copy the current line to line \<number\>
    + yG -> copy the current line to the end of the file
    + yf\<character\> -> copy from the current location of the cursor to the first specified character
    + y\<number\>j -> copy the current line and the next \<number\> lines below
    + y\<number\>k -> copy the current line and the next \<number\> lines above 

PASTING
- p -> paste the last content in the buffer

SUBTITUTION
- :\<beginning line\>,\<ending line\>s/\<pattern to find\>/\<pattern to substitute\>

INDENT
- '\>>' -> indent 1 time
    + \<number\>'>>' -> indent \<number\> line(s) 

CASE-CONVERSION
- U -> upper case (remember use selection mode first)
    + u -> lower case

MACROS
- q\<name of the macro\> -> start recording, press 'q' to stop recording
    + \<number\>@\<name of the recorded macro\> -> play back the recored macro \<number\> times

VISUAL MODE
- v -> selec multiple lines
    + continue to press 'd' -> delete selected lines
    + continue to press '\<number\>>' -> indent \<number\> time(s)
- Ctrl + q -> select multiple lines but at the current cursor only 
    + continue to press 'Shift + i': edit the first selected cursor, press 'Esc' to apply to the others

BUFFERS
- :b \<Tab\> -> list files in buffers

KEYBINDINGS USED IN THIS NEOVIM SETUP
- Ctrl + n -> open a file tree
    + Shift + n -> close the file tree
- Space + ff -> find files starting from the current directory
    + Space + fg -> find files using "live grep"
- Space + gf -> activate formatter of the current file
- Tab -> replace for <CR> (carriage return or "Enter") when having autocompletions
- Space + tt -> open a floating terminal
    + Ctrl + h -> hide a floating terminal
    + Ctrl + D -> exit the current-used terminal
- Shift + k -> hover to get info
- Space + d + t -> toggle breakpoint
- Space + d + c -> start debugger, go to the next breakpoint, exit the ui debugger if there's no more breakpoint

WINDOWS
- Ctrl + w + s -> split the windown horizontally
    + Ctrl + w + v (:vsplit) -> split the window vertically
    + Ctrl + w + c (:split) -> close the current window
- Ctrl + h/j/k/l -> move to the right/bot/top/right window
