---
tags: [Git Tutorial]
title: 3 Setup Git
created: '2019-12-12T12:45:36.362Z'
modified: '2019-12-12T13:28:16.884Z'
---

# 3 Setup Git
There are a lot of settings to customize your Git installation. You can chek them out running

    $ git config --list

For now just take care of you user name and email:

    $ git config --global user.name "Your Name"
    $ git config --global user.email your@email.com

If you like you can also set your editor. If you don't know what that means ignore it for now.

    $ git config --global core.editor vim
