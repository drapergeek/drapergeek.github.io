---
layout: post
title: SSH Config
tags: ssh
published: true
---
Seriously, how did I not know about SSH config before? I've been using SSH regularly for at least 5 years and did not know that a config file existed. I've actually written custom functions to help me out! Do not make the same mistake, use the awesome config file!


The ssh config file lives in your home directory at `~/.ssh/config` and has a very basic format. Check out a simple example here:

```
Host staging
  Hostname staging.example.com
  User deployer
  Port 3333
```

With a simple config file, we can specify an alternate port (handy to avoid people banging on the door all the time), a hostname and a port. Now we can simply call `ssh staging` and it all works perfectly. Compare that to `ssh deployer@staging.example.com -p 3333` and this file becomes nearly magical!

To find more information just check out the [manpage](http://linux.die.net/man/5/ssh_config).
