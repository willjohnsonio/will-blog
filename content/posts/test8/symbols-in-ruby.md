---
slug: symbols-in-ruby-on-rails
date: 2020-03-20
title: What Are Symbols in Ruby on Rails?
description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed molestie leo ut sodales porta. Vivamus pharetra risus ac fermentum faucibus. Nam in sodales ex.'
published: true
author: 'Will Johnson'
---

## What is a symbol in Ruby?

The syntax for symbols is a colon then a word `:symbol`

In Ruby on Rails it's common for symbols to be used to identify methods, instance varibles and hash keys

For example 

```ruby
params.require(:user).permit(:name, :email, :password)
```

`user` is refering to the `@user` instance variable that get created when you create a new user. The `:name`, `:email`, and `:password` symbols refer to the attributes of the User model.

Instead of accessing using `user["password"]` you can use use `password`to make the syntax cleaner.

Symbols can't be changed what the represent will always be the same. Coming from JavaScript where data can be changed often I like this consistancy on my code.

Also, I found out in my research that since every time you call a symbol is call the same object, so it's only one instance running, but with something like a string the same sting will create multiple instances and use more memory. 