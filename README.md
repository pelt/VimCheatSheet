# VimCheatSheet

## General

* Configuration File: ```.vimrc``` (see :set commands)
* Different Modes
** visual
** insert
** command

| Command                  | Explanation |
| ------------------------ | ----------- |
| :help [command]          | open help, optionally for specific command |
| :help tutor              | open tutor |
| &lt;F1&gt;               | open help |
| | |
| &lt;ESC&gt;              | leave mode/cancel operation |
| &lt;number&gt;           | multiply command by &lt;number&gt; |
| &lt;CTRL&gt;+G           | display status about file |
| .                        | repeat last command  |
| J                        | join line |
| | |
| u                        | undo last edit |
| &lt;CTRL&gt;+r           | redo the last undo |
| | |
| q&lt;alpha-character&gt; | start recording of keystrokes, q stops the recoding |
| @&lt;alpha-character&gt; | replay keystrokes stored in register &lt;alpha-character&gt; |
| | |
| :digraphs                | shows available digraph character |
| &lt;CTRL&gt;+k           | insert digraph (in insert mode) |
| | |
| :marks                   | show all marks |
| | |
| !&lt;motion&gt;&lt;external commmand&gt; | filter the selected area by &lt;external command&gt; |
| !!&lt;external commmand&gt; | filter the current line by &lt;external command&gt; |


## Configuration

All Configurations can be disabled with `no` like `:set nonumber`.

| Command        | Explanation |
| -------------- | ----------- |
| :set number    | turn on line numbering |
| :set hlsearch  | turn on highlighting for search matches |
| :set incsearch | turn on incremental searches |
| :set autowrite | turn on writing on closing files like :q |

## Movement

| Command                  | Explanation |
| ------------------------ | ----------- |
| h                        | move cursor left
| j                        | move cursor down
| k                        | move cursor up
| l                        | move cursor right
| w                        | move cursor forward one word
| b                        | move cursor backward one word
| 0                        | move cursor to start of line
| ^                        | move cursor to first nonblank character in line
| $                        | move cursor to end of line
| G                        | move cursor to last line
| &lt;number&gt;G          | move cursor to line &lt;number&gt;
| &lt;CTRL&gt;+U           | move cursor half page up
| &lt;CTRL&gt;+D           | move cursor half page down
| f&lt;character&gt;       | move cursor to next &lt;character&gt; |
| F&lt;character&gt;       | move cursor to last &lt;character&gt; |
| t&lt;character&gt;       | move cursor before next &lt;character&gt; |
| T&lt;character&gt;       | move cursor behind last &lt;character&gt; |
| m&lt;alpha-character&gt; | mark the position and save in &lt;alpha-character&gt; |
| `&lt;alpha-character&gt; | go to mark saved in &lt;alpha-character&gt; |

## Inseration

| Command         | Explanation |
| --------------- | ----------- |
| i               | insert before cursor |
| a               | insert after cursor |
| I               | insert at beginning of line |
| A               | insert at end of line |
| o               | insert new line after current line |
| O               | insert new line before current line |
| p               | put saved changes after cursor/line |
| p               | put saved changes before cursor/line |
| y&lt;motion&gt; | yank (copy) up to &lt;motion&gt; |
| yy              | yank (copy) current line |
| Y               | yank (copy) current line |

## Changing Text (deleting and switch to insert mode)

| Command         | Explanation |
| --------------- | ----------- |
| c&lt;motion&gt; | change all up to &lt;motion&gt; (exception is cw which acts as ce) |
| cc              | change current line |
| C               | change up to end of line (like c$) |
| r               | replace character under cursor |
| ~               | change case (upper/lower characters) |

## Deletion

| Command         | Explanation |
| --------------- | ----------- |
| x               | delete character under cursor |
| dd              | delete line |
| d&lt;motion&gt; | delete all up to &lt;motion&gt; |

## Files

| Command         | Explanation |
| --------------- | ----------- |
| :args           | show which files are open |
| ZZ              | writes and exit file (same as :wq) |
| :w[!]           | writes file [ignores read-only mode] |
| :q[!]           | exit file without writing [without warning] |
| :vi[!] [file]   | close and open file |
| :view[!] [file] | close file and open new one in read-only mode |
| :e[!]           | same as :vi |
| :n[!]           | move to next file |
| :prev[!]        | move to previous file |
| :N[!]           | same as :prev |
| :first[!]       | start edit of first file |
| :rewind[!]      | same as first |
| :last[!]        | start edit of last file |
| CTRL-^          | start edit of last edited file (register `#`)|
| CTRL-6          | same as CTRL-^ |

## Searching

| Command            | Explanation |
| ------------------ | ----------- |
| /&lt;string&gt;    | forward search for &lt;string&gt; |
| ?&lt;string&gt;    | backward search for &lt;string&gt; |
| n                  | jump to next match |
| N                  | jump to next match reverse direction |
| :nohlsearch        | clear highlighting for current search |

## Regular Expressions for Searches

| Character           | Explanation |
| ------------------- | ----------- |
| ^                   | start of line |
| $                   | end of line |
| .                   | single character |
| \\&lt;character&gt; | turn of special meaning of &lt;character&gt; |

# References

* ftp://ftp.vim.org/pub/vim/doc/book/vimbook-OPL.pdf
