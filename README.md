# VimCheatSheet

## General

* Configuration File: ```.vimrc``` (see :set commands)
* Different Modes
** visual
** insert
** command

| Command            | Explanation |
| ------------------ | ----------- |
| :help [command]    | open help, optionally for specific command |
| :help tutor        | open tutor |
| &lt;F1&gt;               | open help |
| | |
| &lt;ESC&gt;              | leave mode/cancel operation |
| &lt;number&gt;           | multiplies commands by &lt;number&gt; |
| &lt;CTRL&gt;+G           | display status about file |
| .                  | repeats last command  |
| J                  | join line |
| | |
| u                  | undo last edit |
| &lt;CTRL&gt;+r           | redo the last undo |
| | |
| q&lt;alpha-character&gt; | start recording of keystrokes, q stops the recoding |
| @&lt;alpha-character&gt; | replay keystrokes stored in register &lt;alpha-character&gt; |
| | |
| :digraphs          | shows available digraph character |
| &lt;CTRL&gt;+k           | insert digraph (in insert mode) |

## Configuration

| Command       | Explanation |
| ------------- | ----------- |
| :set number   | turn on line numbering |
| :set nonumber | turn off line numbering |

## Movement

| Command         | Explanation |
| --------------- | ----------- |
| h               | move cursor left
| j               | move cursor down
| k               | move cursor up
| l               | move cursor right
| w               | move cursor forward one word
| b               | move cursor backward one word
| 0               | move cursor to start of line
| ^               | move cursor to first nonblank character in line
| $               | move cursor to end of line
| G               | move cursor to last line
| &lt;number&gt;G | move cursor to line &lt;number&gt;
| &lt;CTRL&gt;+U  | move cursor half page up
| &lt;CTRL&gt;+D  | move cursor half page down

## Inseration

| Command | Explanation |
| ------- | ----------- |
| i       | insert before cursor |
| a       | insert after cursor |
| I       | insert at beginning of line |
| A       | insert at end of line |
| o       | insert new line after current line |
| O       | insert new line before current line |

## Changing Text (deleting and switch to insert mode)

| Command         | Explanation |
| --------------- | ----------- |
| c&lt;motion&gt; | changes all up to &lt;motion&gt; (exception is cw which acts as ce) |
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

## Closing File

| Command | Explanation |
| ------- | ----------- |
| ZZ      | writes and exit file (same as :wq) |
| :w      | writes file |
| :q      | exit file without writing |
| :q!     | exit file without warning |
| :wq     | write and exit file |

## Searching

| Command            | Explanation |
| ------------------ | ----------- |
| f&lt;character&gt; | move cursor to next &lt;character&gt; |
| F&lt;character&gt; | move cursor to last &lt;character&gt; |
| t&lt;character&gt; | move cursor before next &lt;character&gt; |
| T&lt;character&gt; | move cursor behind last &lt;character&gt; |


# References

* ftp://ftp.vim.org/pub/vim/doc/book/vimbook-OPL.pdf
