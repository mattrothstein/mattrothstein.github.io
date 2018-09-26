---
layout:   post
title:    Frozen String Literal True Vim Command
author:   Matt
category: vim
tags:     vim ruby frozen_string_literal_true command
finished: true
---

### Custom Vim Command

This vim command will insert the ruby magic comment at the top of a file when executed.

```vim
  :command Frt :normal gg O# frozen_string_literal: true<CR><ESC>x
```

Then I map it to `<Space>frt` with this command `map <Space>frt :Frt<CR>`. This saves me a lot of key strokes and allows me to decide when the comment is needed.

