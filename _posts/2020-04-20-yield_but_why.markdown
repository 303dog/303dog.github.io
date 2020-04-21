---
layout: post
title:      "    .Yield (but why?)"
date:       2020-04-21 02:46:46 +0000
permalink:  yield_but_why
---


First, what is a "block" of code?  
Ruby Code blocks are chunks of code between braces or  
between do. .end that you can associate with method invocations.

Because code blocks can often be used mulitple times and in multiple files, we need a way to call it from our methods without needing to type it all out several times. This mechanism allows you to customise a method depending on your needs.

I would like to introduce you to # .yield.  Yield allows us to call on a particular code block from any method we choose.

EXAMPLE:

```
def one_yield
  yield
end

def multiple_yields
  yield
  yield
end

one_yield { puts "one yield" }

multiple_yields { puts "multiple yields" }
```
```
one yield
multiple yields
multiple yields
```

**block_given?**
When yield is called in a method then the method requires a block. Otherwise, a LocalJumpError is raised. Using block_given? allows us to have options.  If we want to use the yield block we can but we dont have too if it's not needed.

```
def optional_block
  yield if block_given?
end

optional_block # => nil
optional_block { puts 'optional block' } # => optional block
```



