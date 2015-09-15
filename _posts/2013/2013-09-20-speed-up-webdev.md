---
layout:     post
date:       2013-09-20 20:00
title:      "Speed Up Web Development"
category:   meaningful-labor
slug:       speed-up-webdev
syntax:     true
---

These are a couple of tips and tricks about how to speed up your web development process. Most of us use basically the same tools: Django or Ruby on Rails, Sass, Git and a nice text editor like Sublime Text, Textmate or Coda.

#### A text editor with plugins support

I highly recommend using Sublime Text because it is not only very fast and has a robust set of features, but because of its plugins support. You have to install <a href="https://sublime.wbond.net/" ref="nofollow">Package Control</a> which is a plugin package manager with an interactive user interface. You also get a repository of plugins with a web based interface. Here are my list of plugins:

* Tag
* Sass
* Smart Match
* TrailingSpaces
* SideBarEnhacements
* SublimeOnSaveBuild
* Soda Light 3 theme

#### Build Sass on file save

You can set up Sublime Text to build Sass on .sass or .scss file saving process. You will need SublimeOnSaveBuild plugin and a build system for Sass. Make sure you did a *gem install sass* before setting up a new build system that looks like this:

    {
        "cmd": ["sass", "-C", "$file:$file_base_name.css"],
        "shell": false
    }

#### Fish shell with inline Git status

Fish is an interactive shell which can be run on top of bash to preserve your bash PATH settings. Autocomplete is not the only magic feature, but it also comes with git status support — but you have to set this up. You have to add the config details to *~/.config/fish/config.fish* file.

    # Fish git prompt
    set __fish_git_prompt_showdirtystate 'yes'
    set __fish_git_prompt_showstashstate 'yes'
    set __fish_git_prompt_showupstream 'yes'
    set __fish_git_prompt_color_branch yellow
    # Status Chars
    set __fish_git_prompt_char_dirtystate '⚡'
    set __fish_git_prompt_char_stagedstate '→'
    set __fish_git_prompt_char_stashstate '↩'
    set __fish_git_prompt_char_upstream_ahead '↑'
    set __fish_git_prompt_char_upstream_behind '↓'
    # Add git to fish prompt
    function fish_prompt
        set last_status $status
        set_color $fish_color_cwd
        printf '%s' (prompt_pwd)
        set_color normal
        printf '%s ' (__fish_git_prompt)
        set_color normal
    end

#### FTP from command line with LFTP

If you want rapid deployment over FTP, a recommend install [lftp](http://lftp.yar.ru) command line tool. It has a mirror function that works pretty well for Jekyll powered sites and blogs. I use it every time I want to push the local changes of this blog to the live site.
