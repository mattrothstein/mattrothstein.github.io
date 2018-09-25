---
layout:   post
title:    Ruby Semicolon
author:   Matt
category: ruby
tags:     ruby semicolon script
finished: true
---

### Suppressing Output in Ruby

I will occasionally have to write scripts to execute in the console. A lot of the time I can't copy and paste the entire script at once because of the long output. For example, code like below will return every `Person` in the collection as output.

```ruby
  people = Person.all
  => [
    #<Person:12345678910
      name: 'person 1',
      created_at: Thu, 18 Jun 2015 10:54:31 EDT -04:00,
      updated_at: Thu, 18 Jun 2015 10:56:21 EDT -04:00>,
    #<Person:12345678911
      name: 'person 2',
      created_at: Thu, 18 Jun 2015 10:54:31 EDT -04:00,
      updated_at: Thu, 18 Jun 2015 10:56:21 EDT -04:00>,
    #<Person:12345678912
      name: 'person 3',
      created_at: Thu, 18 Jun 2015 10:54:31 EDT -04:00,
      updated_at: Thu, 18 Jun 2015 10:56:21 EDT -04:00>,
    #<Person:12345678913
      name: 'person 4',
      created_at: Thu, 18 Jun 2015 10:54:31 EDT -04:00,
      updated_at: Thu, 18 Jun 2015 10:56:21 EDT -04:00>,
  :
```

In this situation you can scroll through the collection to view its contents but you can't execute anymore code until you exit this mode. You will have to press the `Q` key to exit then you can go on with your script. One way to avoid this is to supress the output using a semicolon and paste your entire script without any output.

```ruby
  people   = Person.all;
  children = people.where('age < ?', 18);
  adults   = people.where('age >= ?', 18);
```
Now I can paste these 3 queries in to my console without any need to clear output between lines.
