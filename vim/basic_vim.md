# Vim

## Start 

~~~
$ vimtutor
~~~

## Basic

### **Move**

~~~
h, l, k, j, w, b, e
zz zb zt
$ _ 
shift + g
gg
%: {.....}, (.......), [.......]
Ctrl + o: takes you back to older positions
Ctrl + i: to newer positions 
~~~

### Quit

`q!, wq`

### Edit

~~~
a/A
i
dw/daw/d$/dd
u
Ctrl + r: undo the undo's 
p/P (normal mode)
r/R
o/O
~~~

### Find

~~~
/{pattern}
n/N: next/previous
f{char}/F{char}, switch by using ';/,'
~~~

### Substitute

~~~
:s/old/new, to substitute new for the first old in a line type
:s/old/new/g, to substitute all in a line type
:#,#s/old/new/g
:%s/old/new/g 
:%s/old/new/gc - add 'c' flag on the end to show each match, 'y' substitute this match, 'n' skip this match, 'q' quit substituting, 'l' substitute this match and quit, 'a' substitute all, <C-e> Scroll the screen up, <C-y> Scroll the screen down 
~~~

## Advanced

### Delete in Insert Mode

~~~
Ctrl + w: Insert Mode, Delete back one word 
Ctrl + u: Insert Mode, Delete back to start of line 
~~~

### Change in Insert Mode

~~~
<C-n>/<C-p> - select the previous and next items in the word list (insert mode) 
<C-y>(insert mode) - accept the currently selected match
<C-e>(insert mode) - quit from autocompletion 
<C-h>/<C-l>(insert mode) - delete or add on crrrent match
{char} - stop complete and insert 
~~~

### Visual Mode 

~~~
v/V/Ctrl+v (Choose something, and add some operations. For example, r/c/A in insert mode.)
~~~

### Tab

~~~
:tabe[dit] {filename}
:tabc[lose] 
:tabo[nly] 
:tabn[ext] {N} == {N}gt
:tabn[ext] == gt
:tabp[revious] == gT
~~~

### Windows

~~~
Ctrl + w + s/v
Ctrl + w + w/k/j/h/l
:qa! - Close all windows, discarding changes without warning
:wa - Write all modified buffers to disk
:sp {file}
:vsp {file}
:clo == <C-w>c - Close the active window
:on == <C-w>o - Keep only the active window, closing all others
~~~

### Copy

~~~
:6t. - Copy line 6 to just below the current line
:t6 - Copy the current line to just below line 6
:t. == yyp 
:t$ - Copy the current line to the end of file
:'<,'>t0 - Copy the visually selected lines to the start of the file
V -> :'<,'>m$ - Moving visually selected parts to the end of file
~~~

### History 

~~~
q/ - Open the command-line window with history of searches 
q: - Open the command-line window with history of Ex commands
:sh
:!{cmd}
~~~

### Registers

~~~
"{register}
"a -- "z - The named register 
"0 - The yank register 
"_d{motion} (e.g., "_diw) - Delete the specified text without saving a copy
"= - the expression register
"% - Name of the current file
"# - Name of the alternate file 
". - Last insert text 
": - Last Ex command 
"/ - Last search pattern 
<C-r>{register}(insert mode) - use in insert mode
yt{char} -> <c-r>(insert mode) -> 0 
~~~

### Macro

~~~
q{register}(...)q
q{register}q - clear the register
@{register} 
@@ - repeats the marco that was invoked mostly resently 
qq;.q - 'qq' tells Vim to record the following keystrokes and save them to the 'q' register. Then type commands ';.' and finish recording by type 'q'
~/vU - Change singal letter to uppercase in a word
~~~

## Troubleshooting

### ...

placeholder
