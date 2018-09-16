---
id: vim-notes
title: VIM Notes
sidebar_label: useful vim notes
---

## Interpreting keys

* `dw` In sequence, press d , then w
* `dap` In sequence, press d , a , then p
* `< C-n>` Press < Ctrl> and n at the same time
* ` g< C-]>` Press g , followed by < Ctrl> and ] at the same time
* `< C-r>0` Press < Ctrl> and r at the same time, then 0
* `< C-w>< C-=>` Press < Ctrl> and w at the same time, then < Ctrl> and = at the same time
* `f{char}` Press f , followed by any other character
* `m{a-zA-Z}` Press m , followed by any lowercase or uppercase letter
* `d{motion}` Press d , followed by any motion command
* `<C-r>{register}` Press < Ctrl> and r at the same time, followed by the address of a register
* `<Esc>` Press the Escape key
* `<CR>` Press the carriage return key (also known as <Enter> )
* `<Ctrl>` Press the Control key
* `<Tab>` Press the Tab key
* `<Shift>` Press the Shift key
* `<S-Tab>` Press the <Shift> and <Tab> keys at the same time
* `<Up>` Press the up arrow key
* `<Down>` Press the down arrow key
* `␣` Press the space bar

---
## Moving

* `j` move one line down
* `k` move one line up
* `h` move one character left
* `l` move one character right
* `0` move to beginning of line
* `$` move to end of line
* `w` jump to beginning of next word
* `W` jump to next word based on white space
* `b` jump to beginning of word
* `B` jump to beginning of word based on white space
* `e` jump to end of word
* `E` jump to end of word based on white space
* `ge` jump to end of previous word
* `gj` move one line down in wrapped line
* `gk` move one line up in wrapped line
* `>` indent by shiftwidth space
* `=` auto indent
* `%` jump between matching parentheses
* `gg` move to beginning of file
* `G`  move to last line in file
* `:n` move to line n
* `n+gg` move to line n
* `<C-f>` or `Page Down` move forward one page
* `<C-b>` or `Page Up` move backward one page
* `zt` position the screen with the cursor at the top
* `zz` position the screen with the cursor at the middle
* `zb` position the screen with the cursor at the bottom
* `(` / `)` Jump to start of previous/next sentence
* `{` / `}` Jump to start of previous/next paragraph
* `H` / `M` / `L` jump to top / middle / bottom of window
* `gf` Jump to file name under the cursor


---
## Repeating & Undoing

* `u` undo last change (can be repeated to undo preceding commands)
* `<C-r>` redo last change (insert mode)
* `.` repeat the last change

---
## Editing File

* `yy` yank (copy) the current line
* `y$` yank (copy) to end of line
* `yG` yank (copy) to end of file
* `"+y` yank (copy) to system clippboard
* `Nyy` Yank (copy) N lines and put it in buffer
* `p` paste after cursor
* `P` paste infront of cursor
* `]p` Paste text, aligning indentation with surroundings
* `"+p` paste from system clippboard
* `dd` delete (cut) a line
* `dw` delete the word at the current position
* `d$` delete (cut) to end of line
* `dG` delete (cut) to end of file
* `Ndd` delete N lines
* `x` delete character at current position
* `Nx` delete N characters, starting at current position
* `r` Replace character at current position
* `R` replace text starting with current position
* `a` append text after cursor
* `A` append text at end of current line
* `i` insert text before cursor
* `I` insert text at beginning of current line
* `o` start a new line below current line
* `O` start a new line above current line
* `gg` then `dG` - delete all content
* `cw` deletes to the end of word
* `s` deletes the character under the cursor and then enters Insert mode.
* `<C-a>` perform addition on number (normal mode)
* `<C-x>` perform subtraction on number (normal mode)
* `<C-h>` delete back one character (backspace)
* `<C-w>` delete back one word
* `<C-u>` delete back to start of line

---
## Visual Mode - Selections

* `v` start in visual mode
* `V` line select in visual mode
* `<C-v>` enable block-wise Visual mode
* `gv` reselect the last visual selection
* `o` go to the opposite end of the highlighted text
* `>.` dot command indents on the same selected text block. Hit `.` to repeat indentation.
* `U` upcase selected text

---
## Operator + Text Objects = Combos!

Operators:  
`c` Change
`d` Delete
`y` Yank into register
`g~` Swap case
`gu` Make lowercase
`gU` Make uppercase
`>` Shift right
`<` Shift left
`=` Autoindent
`!` Filter {motion} lines through an external program

Text Objects:  
(w)ord
(s)entence
(p)aragraph
(i)nner
(a)round
(t)ags

* `dw` delete word
* `cw` change word (change to Insert Mode)
* `viw` selects current word
* `vaw` selects current word with a space after
* `diw` delete current word
* `daw` delete current word with a space after
* `dap` delete paragraph with the space after
* `vip` selects paragrah
* `vap` selects paragrah with space after
* `vis` selects sentence
* `vas` selects sentence with space after
* `vit` selects inner content between HTML tags
* `vat` selects inner content including HTML tags
* `cit` change inside the tag (delete content inside HTML tags)
* `vi)` selects content between brackets (you can change to other syntax)
* `va)` selects including brackets
* `vib` selects inside parenthesis "()"
* `viB` selects inside curly braces "{}"
* `fs`  in a line, go to the first "s"
* `vfsr` in a line, visual mode, select the line until the first "s"
* `gUis` capitalize sentence
* `gUip` capitalize paragraph
* `dt{chr}` delete until next specified character


---
## Vim Commands
learn more with `:h ex-cmd-index`  

* `@:` repeat the last command
* `:e` start editing a new file
* `<C-o>` switch from insert mode to normal mode for one command
* `<C-c>` instead of ESC to switch out of insert mode
* `<C-[>` instead of ESC to switch out of insert mode
* `<C-p>` previous word completion (similar word in current file)
* `<C-n>` next word completion (similar word in current file)
* `:r file2` read in file2 and insert at current position
* `:f` current file name
* `:w` write to the file
* `:w myfile` Write out the file to myfile
* `:w! file2` Overwrite file2
* `:x` or `:wq` exit and write out modified file
* `:q` quit 
* `:q!` quit even though modifications have not been saved
* `:vsp` vertically split windows
* `:diffs` split and diff
* `:diffoff` close diff
* `:pwd` show present working directory.
* `:w !ruby -c` check for syntax error in ruby file
* `:w !sudo % tee` write file using sudo with permission
* `:source ~/.vimrc` resourcing vimrc file
* `:source $MYVIMRC` same thing as resourcing vimrc file
* `:set ft?` check filetype of current document
* `:w foobar` save the current file in a new file named foobar
* `:!rm foobar` use the '!' to run system command, removing file foobar
* `:saveas foonew` change and save the current file as foonew
* `vim myfile` start the vim editor and edit the `myfile` file
* `vim -r myfile` start vim and edit myfile in recovery mode from a system crash
* `ga` display cursor charactor in decimal and hexadecimal notations
* `:bp` previous in buffer list
* `:bn` next in buffer list
* `:bd` delete from buffer list
* `:reg` display register
* `:shell` start a shell session
* `:retab` To change all the existing tab characters to match the current tab settings
* `:nmap` viwe currently mapped keys for normal mode. More info `:help map`
* `:vmap` viwe currently mapped keys for visual mode. More info `:help map`
* `:imap` viwe currently mapped keys for insert mode. More info `:help map`


---
## Search

* `/` pattern Search forward for pattern
* `?` pattern Search backward for pattern
* `n` move to next occurrence of search pattern
* `N` Move to previous occurrence of search pattern
* `*` search for the word under the cursor
* `f{char}` count the occurence of {char} to the right in current line. Use `,` and `;` to jump back and forth.
* `:noh` deselect search highlighted words

---
## Panes and tabs
* `<C-w>s` split window horizontally
* `<C-w>v` split window vertically
* `:sp {file}` load a file into horizontal split windows. `TAB` to help navigate files
* `:vsp {file}` load a file into veritically split windows. `TAB` to help navigate files
* `￼<C-w>c` or `:cl` close the active window
* `<C-w>o` or `:on` keep only the active window, closing all others
* `:tabe {filename}` open {filename} in a new tab
* `:tabc` close the current tab page and all of its windows
* `:tabo` keep the active tab page, closing all others
* `<C-w>R` swap top/bottom or left/right split
* `<C-w>T` break out current window into a new tabview
* `<C-w>o` close every window in the current tabview but the current one


---
## Unusual Characters
see more using `:h digraphs-default` && `:h i_CTRL-V_digit`
* `<C-v>065` insert "A" by character code
* `<C-k>?I` insert “¿” character (under insert mode)
* `<C-k>14` insert fraction 1⁄4


---
## Vim Settings (.vimrc)

You can change settings directly within vim using commands.
There are tons of shortcuts for vim settings. For example, `bg` is short for `background`. It's a good way to quickly switch things on and off when in vim. However, it's recommended to use full name in the `.vimrc` file for readability purposes.

Enter a non boolean setting without options to see what it's currently set to.
E.g., `set background` #=> `background=light`

For boolean settings, you can use the `?` trailing to see the current setting.
E.g., `set relativenumber?` #=> `norelativenumber`


`set number` set number line.
`set relativenumber` set line number based on position of cursor
`set numberwitdh` set width of number column
`set nonumber ` turn number off by adding 'no' infront of the command
`set number!` toggle option, will turn setting on and off
`set background=dark`
`set background=light`
`set textwidth=50` - setting the width of each line to be 50 chars.
`set linebreak` - useful when wrap is on so text doesn't get cut off at each line.
`set showbreak` - show where the lines are wrapped with '>'.


#### Filetype Event

.vimrc:

```
syntax on
filetype indent on
set smartindent

autocmd BufRead,BufWritePre *.html normal gg=G

**HTML files will be automatically formatted before saving to disk.
```




#### Custom Auto Comment
```
autocmd Filetype html nnoremap <leader>c I<!--<esc>A--><esc>
**in html file, when pressed "\c" it'll execute the command and put <!-- and --> on either side of the line

autocmd Filetype javascript nnoremap <leader>c I//<esc>
**similar to above, will insert javascript comment in a javascript file
```


#### Auto Command Groups
```
augroup JavaScriptCmds
        autocmd!
        autocmd Filetype .....
        autocmd Filetype javascript setlocal.....
        .......
augroup END
```


#### Set Variables

`let` is used to set variables in vim script.

`let mapleader=','` setting the leader key '\' to comma key','

`:map` - see current mapping

You can disable the arrow keys in your .vimrc to force yourself to use vim  without using them :)
```
noremap <left> <nop>
noremap <right> <nop>
noremap <up> <nop>
noremap <down> <nop>
```

comments starts with a quotation mark

`"` this is a comment in vim



### Local Settings 

When you are working with different filetypes, sometimes it's a bit more convenient to use `setlocal` to apply specific settings to those filestypes.


`autocmd Filetype ruby setlocal tabstop=2 softtabstop=2 shiftwidth=2` setting tab spaces when handling ruby files
`autocmd Filetype javascript setlocal tabstop=4 softtabstop=4 shiftwidth=4` setting tab spaces when handling javascript files
`autocmd Filetype html setlocal tabstop=2 softtabstop=2 shiftwidth=2` setting tab spaces when handling html files

`setlocal nowrap` - set no wrap only to current file




---
## Resources  
http://blog.interlinked.org/tutorials/vim_tutorial.html  
https://pragprog.com/book/dnvim/practical-vim  
http://vimcasts.org/categories/  
http://everythingsysadmin.com/2010/09/a-powerful-vim-command-i-never.html  
http://worldtimzone.com/res/vi.html  
http://stackoverflow.com/questions/235839/indent-multiple-lines-quickly-in-vi  
http://usevim.com/2012/04/13/registers/  
https://www.cs.oberlin.edu/~kuperman/help/vim/home.html  
http://usevim.com/  
https://robots.thoughtbot.com/vim-splits-move-faster-and-more-naturally  