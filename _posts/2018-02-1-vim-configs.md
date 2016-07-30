---
layout:   post
title:    Customizing VIM
author:   Matt
category: vim
tags:     vim keys config .vimrc
finished: true
---

### Customizing your VIM setup

I had originally started my editor journey with Atom, then explored vim and fell in love with modal editing. After using vim for a few months I saw a co-worker using spacemacs and was impressed with all it did. It did everything that vim did and a little more, so I started using spacemacs and didn't look back.

I started to realize that spacemacs taking longer to start up than vim ever did and I was having a hard time setting it up on another computer. Vim worked on that machine, cause vim always works, so i just used vim on my personal machine and spacemacs at work. I started modifying my vim config to behave more like spacemacs so I could do things with the same commands.

One of the things about spacemacs that I really enjoyed was the spacebar being the leader key. So I mapped a bunch of commands to behave the same way in vim as they do in spacemacs. For example:

```vim
  map <Space>ff :FZF<CR>
  map <Space>gb :Gblame<CR>
  map <Space>nt :NERDTreeToggle<CR>
  map <Space>nf :NERDTreeFind<CR>
  map <Space>bb :ls<CR>
  map <Space>as :AS<CR>
  map <Space>a  :A<CR>
  map <Space>rs :RS<CR>
  map <Space>r  :R<CR>
  map <Space>vs :vsplit<CR>
  map <Space>hs :split<CR>
  map <Space>hs :split<CR>
  map <Space><Tab> :b#<cr>
```

Through the use of many available vim plugins and some custom key mappings I was able to do everything I did in spacemacs with vim and not sacrifice any real speed. Vim was still much faster.

In my endless attempts to optimize my setup and find the best editor I know will be modifying my vim config to more effeciently do things.
