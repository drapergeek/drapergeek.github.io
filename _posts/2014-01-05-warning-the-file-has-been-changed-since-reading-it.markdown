---
layout: post
title: 'WARNING: The file has been changed since reading it!'
published: true
tags: vim
---

Papercuts, hitting your pinky toe, and that message have to rank among the most
annoying things that can happen to a human being!

Here is a simple trick that can cut down on how often you see that
message.

You've changed branches or you've done a rebase; when you move back into VIM
just toss in:

```
:windo e!
```
This will tell VIM to edit all the buffers in the current window using their
current file. This forces a reload of all your files so that if anything changed, you
will see the most recent version of the file and VIM won't complain that it has
changed since you last read it.

You can save yourself a bit more work by tossing in an alias such as ge (git
edit):

```
map <Leader>ge :windo e!<CR>
```

Hopefully this can save you a tiny bit of annoyance!
