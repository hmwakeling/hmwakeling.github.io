---
title: 'How to get emacs back in your terminal after upgrading to macOS Catalina'
date: 2019-11-12
permalink: /posts/2019/11/blog-post-2/
tags:
  - macOS Catalina
  - emacs
  - GNU
  - terminal
---

### How to get emacs back in your terminal after upgrading to macOS Catalina.

So you've upgraded to macOS, but things have changed. Your trusty old emacs is no longer bundled in the operating system and you know ALL of the shortcuts and just don't want to change to vim (ugh).

Luckily, the fix is simple!

Head to [https://emacsformacosx.com/](https://emacsformacosx.com/) to download emacs to your mac and store it in `~/Applications`.

Head to your Terminal and in your home directory open (using vim for the last time!) your .zshrc file. (To edit a vim file type 'i' first.)
`> vim .zshrc`

(If you don't have one already, simple make one first!
`> touch .zshrc`
)

Add the line
`> alias emacs="/Applications/Emacs.app/Contents/MacOS/Emacs -nw"`
The -nw argument enables it to open in your terminal window and not a new one.

Now exit out of vim (`:wq`), source your .zshrc file (`source ~/.zshrc`), and run emacs!
`> emacs yourFileName.ext`


A quick extra tip: If you were a bash user and want your `.bash_profile` settings back, you could simply add
`source ~/.bash_profile`
to your .zshrc file and get most of your preferences back!