# Vim Cheatsheet

## fold and unfold

```
za :open a fold under cursor
zA :open a fold under cursor
zm: increase one fold level 
zM: fold all
zr: decrease one fold level
zR: unfold all
zo: open fold at cursor
zO: open all fold at cursor
zj: move to next fold
zk: move to previous fold
zi: invert 'foldenable'
```

## vimgrep in current file

```
vimgrep /pattern/ %
```

## vimgrep in current folder

```
vimgrep /pattern/ *
```

## quickfix

```
open: copen
next: cnext
previous: cprev
```

## current date

```
:r !date
```

actually you can always run the shell command in VIM and insert the outputs like this

zsh:1: command not found: data

```
:r !command
```

## change to current folder

```
:cd %:h

%   full path to current path
%:h full path to current file without filename itself
```

## substitute

```
:%s/foo/bar/g   find and replace in all line
:s/foo/bar/g    find and replace in current line
:%s/foo/bar/gc    find and replace in current line and ask for confirmation
:%s/foo/bar/gci    find and replace in current line, ask for confirmation, case insensative
```

## edit command line


:<Ctrl-f> to edit the command line with vim normal mode

q:, q/, q?, edit, search in command line

## autocomplete

^x^n    for just this file
^x^f    for filenames
^x^]    for tags
^x      for anything specified by the 'complete' option

## command line

@:      run last command

## scroll

zt or z<CR> put current line at top of window
zz or z.    put current line at center of window
zb or z-    put current line at bottom of window

## fiename modifiers

http://vimdoc.sourceforge.net/htmldoc/cmdline.html#filename-modifiers
