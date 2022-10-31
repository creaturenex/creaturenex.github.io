---
layout: post
title:  "Thoughtbot's Upcase TDD exercise issue with elementary os"
date:   2022-10-31 19:00:00 -0400
categories: linux tdd issue
---

Today I was trying to complete [Thoughtbot's Upcase Fundamental of TDD Exercise](https://thoughtbot.com/upcase/practice) and ran into an issue after I cloned the repo. I tried to run the command `bin/setup` but it was not completed because the logs said I needed to use ruby 2.6. So I thought no problem, I'll used rvm - a ruby version manager. I ran the command `rvm install 2.6` but got an error because one of my ppa repository was returning a 404 error. Specifically
```
Err:8 https://download.docker.com/linux/ubuntu jolnir Release
  404  Not Found [IP: 13.249.190.49 443]
```

This was an annoying issue to troubleshoot because I use elementary os, a ubuntu based distro, which has its own distro name ie jolnir. Because elementary, does not have native docker support it was added to the repo list manually. The repo list are `/etc/apt/sources.list` and `/etc/apt/sources.list.d/docker.list`. In the latter list, the distro was listed as `jolnir` and not `focal`. I decided to view both list with `nano` a terminal editor per this [post](https://stackoverflow.com/questions/41133455/docker-repository-does-not-have-a-release-file-on-running-apt-get-update-on-ubun). After a quick edit to correctly reference `focal`, and rerunning the commands to install ruby 2.6, `bin/setup` was able to be completed as intended.

Now to finish up this exercise!
