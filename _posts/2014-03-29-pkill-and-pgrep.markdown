---
layout: post
title: pkill and pgrep
published: true
---

How often do you find yourself doing something like this?

```
ps aux | grep 'myprocess'
#find the process id

kill -9 2414
```

While working with [Pat Brisbin](http://twitter.com/patbrisbin) the other day, I
done this same thing and he taught me a great shortcut. There are built in
shortcuts for both of these functions.

If you only want to find the process information, you can use `pgrep -f
myprocess`. This does the same thing as ps and then piping that to grep. If you
want to actually kill a process you can shorten it all the way to simply `pkill
 -f my_process`.

I've been wasting my time with extra commands for way too long!
