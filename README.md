# Happy Hacking #

### link to ###

```sh
$ ln -s ~/dotfiles/_vimrc ~/.vimrc
$ ln -s ~/dotfiles/_nvimrc ~/.config/nvim/init.vim
$ ln -s ~/dotfiles/_tmux ~/.tmux.conf
# Linux
$ ln -s ~/dotfiles/_gitconfig_linux ~/.gitconfig
$ ln -s ~/dotfiles/_zshrc_linux ~/.zshrc
# Mac
$ ln -s ~/dotfiles/_gitconfig_mac ~/.gitconfig
$ ln -s ~/dotfiles/_zshrc_mac ~/.zshrc
```

### install fonts ###

$ cp ~/vimrc/font/Monaco.ttf ~/.local/share/fonts
$ cp ~/vimrc/font/MonacoForPowerline.ttf ~/.local/share/fonts
$ fc-cache -vf

### dependencies ###

+ https://github.com/ggreer/the_silver_searcher

### excellent tutorial ###

+ [Practical Vim](https://www.amazon.com/dp/1680501275/ref=olp_product_details?_encoding=UTF8&me=)
+ [Learn vim script the hard way](http://learnvimscriptthehardway.stevelosh.com/)

### tips ###

%s//gc               # search the pattern before you replace it.
%s///gn              # can calculate how many matching in this file
%s/\r//g             # delete all ^M
z<CR>                # scroll
set ff=unix          # change line break to unix style
e ++enc=cp936        # open file with specific encoding (for instance, cp936)

history | vim -      # read from stdin

# disable keyboard in mac
sudo kextunload /System/Library/Extensions/AppleUSBTopCase.kext/Contents/PlugIns/AppleUSBTCKeyboard.kext/
sudo kextload /System/Library/Extensions/AppleUSBTopCase.kext/Contents/PlugIns/AppleUSBTCKeyboard.kext/

+ Gvim be you git default editor and gvimdiff as difftool

```
# should use command *git difftool*, *git mergetool* instead.
$ git config --global core.editor "gvim -f"
$ git config --global diff.tool    gvimdiff
$ git config --global merge.tool   gvimdiff
$ git config --global difftool.prompt false
```

+ Mvim be you git default editor, difftool and mergetool

```sh
$ git config --global core.editor "mvim -f"
$ git config --global merge.tool mvimdiff
$ git config --global mergetool.mvimdiff.cmd 'mvim -df $BASE $LOCAL $REMOTE $MERGED'
$ git config --global diff.tool mvimdiff
$ git config --global difftool.mvimdiff.cmd 'mvim -df $LOCAL $REMOTE'
$ git config --global difftool.prompt false
```
