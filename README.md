# VimCheatSheet


## General

* Configuration File: ```.vimrc``` (see :set commands)
* Different Modes
** normal
** command
** visual
** insert

| Command                  | Explanation |
| ------------------------ | ----------- |
| F1                       | open help |
| :help [command]          | open help, optionally for specific command |
| :help tutor              | open help for tutor |
| | |
| ESC                      | leave mode/cancel operation |
| CTRL-c                   | synonym for ESC |
| CTRL-[                   | synonym for ESC |
| &lt;number&gt;           | multiply command by &lt;number&gt; |
| CTRL+G                   | display status about file |
| .                        | repeat last command  |
| | |
| q&lt;alpha-character&gt; | start recording of keystrokes, q stops the recoding |
| @&lt;alpha-character&gt; | replay keystrokes stored in register &lt;alpha-character&gt; |
| | |
| K                        | look up keyword under cursor (default: man) |


## Configuration

All Configurations can be disabled with `no` like `:set nonumber`.

| Command                        | Explanation |
| ------------------------------ | ----------- |
| :set number                    | turn on line numbering |
| :set hlsearch                  | turn on highlighting for search matches |
| :set incsearch                 | turn on incremental searches |
| :set autowrite                 | turn on writing on closing files like :q |
| :set hidden                    | closing a file will :hide that |
| :set switchbuf=&lt;string&gt;  | control the switch buffer behavior (useopen, usetab, split, vsplit, newtab) |
| :set shiftwidth=&lt;number&gt; | set shiftwidth to &lt;number&gt; (default: tabstop) |


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
| CTRL+U                   | move cursor half page up
| CTRL+D                   | move cursor half page down
| f&lt;character&gt;       | move cursor to next &lt;character&gt; |
| F&lt;character&gt;       | move cursor to last &lt;character&gt; |
| t&lt;character&gt;       | move cursor before next &lt;character&gt; |
| T&lt;character&gt;       | move cursor behind last &lt;character&gt; |
| :marks                   | show all marks |
| m&lt;alpha-character&gt; | mark the position and save in &lt;alpha-character&gt; |
| `&lt;alpha-character&gt; | go to mark saved in &lt;alpha-character&gt; |
| CTRL-]                   | jump to the definition (tag) under the cursor |


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
| P               | put saved changes before cursor/line |
| y&lt;motion&gt; | yank (copy) up to &lt;motion&gt; |
| yy              | yank (copy) current line |
| Y               | yank (copy) current line |
| :digraphs       | shows available digraph character |
| CTRL+k          | insert digraph (in insert mode) |


## Changing Text

| Command                                  | Explanation |
| ---------------------------------------- | ----------- |
| u                                        | undo last edit |
| CTRL+r                                   | redo the last undo |
| J                                        | join line with space |
| gJ                                       | join line withou space |
| c&lt;motion&gt;                          | change all up to &lt;motion&gt; (exception is cw which acts as ce) |
| cc                                       | change current line |
| C                                        | change up to end of line (like c$) |
| r                                        | replace character under cursor by a character |
| s                                        | substitude (synonym for cl) |
| S                                        | substitude line (synonym for cc) |
| ~                                        | change case (upper/lower characters) |
| !&lt;motion&gt;&lt;external commmand&gt; | filter the selected area by &lt;external command&gt; |
| !!&lt;external commmand&gt;              | filter the current line by &lt;external command&gt; |
| >&lt;motion&gt;                          | indent all line in &lt;motion&gt; |
| >>                                       | indent current line |
| <&lt;motion&gt;                          | reverse indent all line in &lt;motion&gt; |
| <<                                       | reverse indent of current line |
| =&lt;motion&gt;                          | indents all lines in &lt;motion&gt; by indent program |
| ==                                       | indents current line by indent program |


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
| ZZ              | writes and exit file (synonym for :wq) |
| :w[!]           | writes file [ignores read-only mode] |
| :q[!]           | exit file without writing [without warning] |
| :vi[!] [file]   | close and open file |
| :view[!] [file] | close file and open new one in read-only mode |
| :e[!]           | synonym for :vi |
| :n[!]           | move to next file |
| :prev[!]        | move to previous file |
| :N[!]           | synonym for :prev |
| :first[!]       | start edit of first file |
| :rewind[!]      | synonym for :first |
| :last[!]        | start edit of last file |
| CTRL-^          | start edit of last edited file (register `#`)|
| CTRL-6          | synonym for CTRL-^ |


## Windows

Commands that close the file will also close the window.

| Command                     | Explanation |
| --------------------------- | ----------- |
| :[size]split [+cmd] [file]  | split the window horizontally |
| :[size]vsplit [+cmd] [file] | split the window vertically |
| :new                        | same as :split but opens a new file |
| :vnew                       | same as :vsplit but opens a new file |
| :sview                      | same as :split but opens in read-only mode |
| CTRL-Ww                     | jump to the next window |
| CTRL-Wj                     | jump to the lower window |
| CTRL-Wk                     | jump to the upper window |
| CTRL-Wh                     | jump to the left window |
| CTRL-Wl                     | jump to the right window |
| CTRL-Wc                     | close current window |
| CTRL-W+                     | increase window size |
| CTRL-W-                     | decrease window size |
| CTRL-W=                     | make all windows the same size |
| [size]CTRL-W_               | make current window [size] (or maximal) lines |


## Buffers

| Command                      | Explanation |
| ---------------------------- | ----------- |
| :buffers                     | show all buffers |
| :buffer &lt;number/file&gt;  | show buffer &lt;number/file&gt; |
| :sbuffer &lt;number/file&gt; | split window and show buffer |
| :bnext                       | show next buffer |
| :sbnext                      | split and show next buffer |
| :bprevious                   | show previous buffer |
| :sbprevious                  | split and show previous buffer |
| :bNext                       | synonym for :bprevious |
| :sbNext                      | synonym for :sbprevious |
| :blast                       | show last buffer |
| :sblast                      | split and show last buffer |
| :brewind                     | show first buffer |
| :sbrewind                    | split and show first buffer |
| :bmodified                   | show modified buffer |
| :sbmodified                  | split and show modified buffer |


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


## Visual Mode

Switching from one visual mode to another is also possible.

| Character | Explanation |
| --------- | ----------- |
| v         | enter visual cursor mode |
| V         | enter visual line mode |
| CTRL-v    | enter visual block mode |
| d         | delete highlighted text |
| D         | delete highlighted lines |
| y         | yank highlighted text |
| Y         | yank highlighted lines |
| c         | change highlighted text |
| s         | synonym for c |
| C         | change highlighted lines |
| S         | synonym for C |
| R         | synonym for C |
| J         | join highlighted lines separated by spaces |
| gJ        | join highlighted lines without separatation |
| r         | replace highlighted text by a character |
| K         | look up highlighted text as a keyword |
| >         | indent highlighted lines |
| <         | reverse indent highlighted lines |
| =         | indent highlighted lines by indent program |
| CTRL-]    | jump to the definition (tag) of the highlighted text |

### Visual Block Mode

| Character | Explanation |
| --------- | ----------- |
| I         | insert left from the block on each line |
| c         | replace the block on each line |
| C         | replace the block up to end of line on each line |
| A         | insert right from the block on each line |
| r         | replace the highlighted block |
| >         | indent left from the block |
| <         | indent right from the block |


# References

* ftp://ftp.vim.org/pub/vim/doc/book/vimbook-OPL.pdf
