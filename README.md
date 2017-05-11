# VimCheatSheet

## General

* Configuration File: ```.vimrc``` (see :set commands)
* Different Modes
** visual
** insert
** command

:help [command] ... open help, optionally for specific command
:help tutor ... open tutor
<F1> ... open help

<ESC> ... leave mode/cancel operation
<number> ... multiplies commands by <number>
<CTRL>+G ... display status about file
. ... repeats last command 
J ... join line

u ... undo last edit
<CTRL>+r ... redo the last undo

q<alpha-character> ... start recording of keystrokes, q stops the recoding
@<alpha-character> ... replay keystrokes stored in register <alpha-character>

:digraphs ... shows available digraph character
<CTRL>+k ... insert digraph (in insert mode)

## Configuration

:set number ... turn on line numbering
:set nonumber ... turn off line numbering

## Movement

h ... move cursor left
j ... move cursor down
k ... move cursor up
l ... move cursor right
w ... move cursor forward one word
b ... move cursor backward one word
0 ... move cursor to start of line
^ ... move cursor to first nonblank character in line
$ ... move cursor to end of line
G ... move cursor to last line
<number>G ... move cursor to line <number>
<CTRL>+U ... move cursor half page up
<CTRL>+D ... move cursor half page down

## Inseration

i ... insert before cursor
a ... insert after cursor
I ... insert at beginning of line
A ... insert at end of line
o ... insert new line after current line
O ... insert new line before current line

## Changing Text (deleting and switch to insert mode)

c<motion> ... changes all up to <motion> (exception is cw which acts as ce)
cc ... change current line
C ... change up to end of line (like c$)
r ... replace character under cursor
~ ... change case (upper/lower characters)

## Deletion

x ... delete character under cursor
dd ... delete line
d<motion> ... delete all up to <motion>

## Closing File

ZZ ... writes and exit file (same as :wq)
:w ... writes file
:q ... exit file without writing
:q! ... exit file without warning
:wq ... write and exit file

## Searching

f<character> ... move cursor to next <character>
F<character> ... move cursor to last <character>
t<character> ... move cursor before next <character>
T<character> ... move cursor behind last <character>


# References

* ftp://ftp.vim.org/pub/vim/doc/book/vimbook-OPL.pdf
