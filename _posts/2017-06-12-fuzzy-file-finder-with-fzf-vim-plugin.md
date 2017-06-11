---
layout: post
title:  "Fuzzy file finder with fzf vim plugin"
date:   2017-06-12
categories: vim, ctr-p, fzf
---

I've been on and off with VIM since I switched to Atom editor but for me, It's bloated. So, here I am again back with VIM and there is so much stuff changed. I recently upgraded to version 8 and it was fast! So I checked out my existing `.vimrc` and replace my plugin manager with [vim-plug](https://github.com/junegunn/vim-plug). I heard a lot of good stuff with [fzf](https://github.com/junegunn/fzf) which is a file fuzzy finder for the terminal, There's a VIM [fzf plugin](https://github.com/junegunn/fzf) so I installed it.

I'm always using [CTRL-P](https://github.com/kien/ctrlp.vim) plugin for fuzzy file finder and it works well But, for some weird reason, it's not working how I wanted it to be. So, I've uninstalled it and replaced it with fzf plugin. However, there's no direct way on how to map :FZF or :Files command or maybe it just me. So, I read the manual and learn about vim's `:noremap` command. Since my memory muscle is wired in already to CTRL + P keys I've re-mapped it to `:FZF` using the configuration  below.

```
noremap <C-P> :FZF<CR>
```
Using CTRL+P as FZF in action
![FZF command in action](http://127.0.0.1:4000/assets/images/fzf-vid.gif)

P.S additional fzf config for layout and to not search what's in your `.gitignore`

```
let g:fzf_layout = { 'down': '~20%' }
let $FZF_DEFAULT_COMMAND = 'ag --hidden --ignore .git -g ""'
```
