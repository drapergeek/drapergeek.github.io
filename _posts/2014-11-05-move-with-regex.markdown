---
layout: post
title: Move with regex
published: true
---

Let's say you want to move a file between two adjacent folders. The most
straightforward way would be as such:

```
mv ~/app/models/builder.rb ~/app/services/builder.rb
```

For years now, this is how I moved my files. Then I paired with a coworker who
gave me a strange look when I ran this command. In ZSH there is a faster way to
make this change:

```
mv ~/app/{models,services}/builder.rb
```

Using the glob `{models,services}` ZSH will make the exact same move with nearly
half the typing! This is all made possible through the wonderful power of
[expansion].

There are so many more tricks available in the shell, it is well
worth some time spent reading the manpages!

[expansion]: http://zsh.sourceforge.net/Doc/Release/Expansion.html
