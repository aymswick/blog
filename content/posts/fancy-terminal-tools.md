---
title: "Does Your Terminal Spark Joy?"
tldr: "Helpful reimaginings of classic Unix tools."
date: 2020-05-20T21:19:27-07:00
draft: false
---
While the list of development tools we have to choose from grows every day, the
humble unix terminal beckons us with simplicity and the promise of a
distraction-free experience. Once you've conquered the initial learning curve
of navigating a command-line interface, you may be craving some sugary features
you gave up ditching IDEs (Integrated Development Environments). Surely there
must be some middle ground between a lone blinking cursor and clunky GUIs
(Graphical User Interfaces)!

Read ahead for some helpful *reimagininings* of classic Unix tools.

## 1. man & tldr
First I'd like to share the [**tldr**](https://tldr.sh/) command, which provides a "just get me up
and running" familiarity with many unix commands. Inspired by the **man**
command to read manual pages for a program, tldr is much more concise and shows
common one-line examples of how a program is used. Yes, you should still read
the man page, but this can save you some time. 

Compare the results below for Hugo, a static site generator:

```
$ man hugo
```


{{< figure src="/images/man-hugo.gif" height="65%" width="70%" >}}

lots of info there...could be a while!

```
$ tldr hugo
```

There we go! Immediately I know how the developer of hugo intends me to use it -
just type **hugo new site** in any directory I'd like to create my website.


{{< figure src="/images/tldr-hugo.gif" height="65%" width="70%" >}}


## 2. Cat -> Bat
The [**Cat**](http://man7.org/linux/man-pages/man1/cat.1.html) command is pretty much
unavoidable when working with the terminal - it allows concatenation of files
(and printing them to standard output) and is the most common way to simply
spit out the contents of a file! 

If I wanted to see the contents of a JavaScript file, I would simply:

```
$ cat example.js
```

and we would get the contents of the file, simply and without fanfare:

{{< figure src="/images/cat.gif" height="65%" width="70%" >}}

This is great, but the [**bat**](https://github.com/sharkdp/bat) command improves
readability of code by adding line numbers and syntax highlighting, all without
sacrificing POSIX compatibility for piping into other programs.

```
$ batcat example.js
```
{{< figure src="/images/bat.gif" height="65%" width="70%" >}}

Awesome! It even opens in a pager (like the *less* command) for vertical
scrolling. If you want this functionality by using the same keyword - cat - you
can set up an alias in your shell. I use [zsh](http://www.zsh.org/), and have
aliased bat as follows:

```bash
alias cat="batcat -n --color auto --style full"
```


## 3. du -> dust
The *du* command shows disk usage and can be used to determine which
directories are taking up the most space - useful when you've run out of said
space! 

```
$ du
```

{{< figure src="/images/du.gif" height="65%" width="70%" >}}

er, ok, looks like we are listing folders and files with numbers prepended to
their entries. Hmm. You can see that it's gonna take some grokking to make sense of this
data.

Let's try the rust replacement, [**dust**](https://github.com/bootandy/dust) - like du but more intuitive, (straight from the
tool website)!

```
$ dust
```
{{< figure src="/images/dust.gif" height="65%" width="70%" >}}

Wow, right away we are given a hierarchical view of the items within the
Downloads folder - accompanied by a graph of size by percentage - or how much of
the total folder size each subfolder is responsible for. Neat! Looks like that
recent free dump of [Springer Textbooks](https://www.springer.com/us) is taking
up 68%! Do I really need *all* those books??

Dust is great for finding size of files, but how about our primary interface
for dealing with files and directories in the shell?


## 3. ls -> exa
ls is the simple "show me what you got" program to list all items in a
directory. It has some helpful options to enable showing hidden/dot files, file
sizes, permissions, and more. The below example will show off listing all
(including hidden) files in the **-l** long format to get those other items I
mentioned.

```
$ ls -la --color
```
{{< figure src="/images/ls.gif" height="65%" width="70%" >}}

This looks all right, and **ls** is pretty configurable as far as output formats.
However, with [**exa**](https://the.exa.website/) we get some enhanced color and
sane defaults.

```
$ exa -la
```
{{< figure src="/images/exa.gif" height="65%" width="70%" >}}

See how the permissions and owners are also color-coordinated? Nice. The exa
website also notes that exa runs in parallel, so you might see much faster
performance working in huge directories.

Those are just a few handy tools I've been exposed to recently that I think
might help you. The year is 2020, and we can live in whatever time we want -
a splash of 1970 with [Cool Retro
Term](https://github.com/Swordfish90/cool-retro-term) mixed with powerful 2020
tools! If you enjoyed this post, please let me know, and if you have any
questions or noticed a mistake, feel free to reach out! If you read through
this blog post and thought, man, I've already known about these for years and I
breezed through this refresher, kudos to you, friend! But I've got something
for you too - check out [Nushell](https://www.nushell.sh/), it fits the theme
of this blog post but expands it to the whole shell itself. Nushell touts
composable tables as the primary method of interaction as opposed to totally
unstructured text.
