---
layout:   post
title:    Get Objects From Memory
author:   Matt
category: ruby
tags:     ruby memory garbage_collector
finished: true
---

### Get all objects of a class that exist in memory

Today I ran into a situation where I needed to have an instance of a class that only existed in memory. Specifically I needed an instance of `File`. The file was generated in a background job and I was not sure where it was saved. With no specific place to look I was able to use `ObjectSpace` module, part of ruby's `GarbageCollector`, to traverse all living instance of `File`.

```ruby
  ObjectSpace.each_object(File).to_a
  => [
    #<File:/Users/matt/file_1.md (closed)>,
    #<File:/Users/matt/file_2.md (closed)>,
    #<File:/Users/matt/file_3.md (closed)>,
    #<File:/Users/matt/file_4.md (closed)>,
    #<File:/Users/matt/file_5.md (closed)>,
    #<File:/Users/matt/file_6.md (closed)>
  ]
```

In using that I was able to find the file I needed.
