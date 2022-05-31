---
title: "Setting up a Coding Environment - Part 2: Customizing VIM with plugins and tuning settings"
date: 2022-05-31
showToc: false
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
draft: false
tags: [Tutorial, VIM]
---

# Introduction

In the first post of this series, we saw how to install and get around VIM. In this post, we will start configuring VIM to our preferences via plugins. All plugins and configurations for VIM are defined in a file called `vimrc`. The file is by default located in your home directory as `~/.vimrc`. This is the file which we edit below.

There are many plugin managers like __vim-plug__, __vundle__ or __minpac__. I recommend using __minpac__ for its simplicity to set up.

# Setting up minpac 

Following the README file from the official github repository, we can install minpac via

```
git clone https://github.com/k-takata/minpac.git ~/.vim/pack/minpac/opt/minpac
```

We should then add the following to the the `vimrc` file:

```
packadd minpac
call minpac#init()
call minpac#add('k-takata/minpac', {'type': 'opt'}) 

" Add some additional plugins below
call minpac#add('davidhalter/jedi-vim')

command! PackUpdate call PackInit() | call minpac#update()
command! PackClean  call PackInit() | call minpac#clean()
command! PackStatus packadd minpac | call minpac#status()
```

After saving the file with `:write`, we can resource the configuration file with `:source %` and then call `:Packpdate`. This will install of the desired plugins if they have not been installed yet and update existing ones. `:PackClean` can be used to remove plugins removed from the `vimrc` file.

# Defining some custom commands

I like to reset the _leader_ key to the space bar. This can be achieved with:

```
let mapleader="\<Space>"
```

Other custom commands can be defined with the `nnoremap` command. Below is an example for how to invoke the fuzzy finder with _Ctrl-f_ and _Ctrl-p_:
```
" Map Ctrl-f and Ctrl-p to FZF
nnoremap <C-f> :<C-u>Files<CR>
nnoremap <C-p> :<C-u>GFiles<CR>
```

# Changing the colorscheme

Colorscheme can be installed in the same way as plugins. I really like the __onedark__ theme, and it can be added via:
```
call minpac#add('joshdick/onedark.vim', {'name': 'onedark'})
packadd! onedark

colorscheme onedark
```

The colorscheme should be changed to the onedark theme now :)
