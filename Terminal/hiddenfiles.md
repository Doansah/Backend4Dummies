### Hidden Files

Hidden Files are quite self-explanatory. They are files that are hidden (duh), but they are REALLY important in software development. Here are the most common ways you'll interact with them. This applies to directories as well.

### Syntax

The rule is dead simple: **if the name starts with a dot, it's hidden.** That's the whole trick.

Files

`.filename.extension`

e.g.

```
.superhiddenfile101.txt
.bashrc
```

Directories

`parent/.directoryname`

e.g.

```
home/.superhiddenDirectory
desktop/folders/.superhiddenphotos
```

### How do I actually see them?

By default `ls` won't show them, that's the point. Add the `-a` (all) flag:

```
ls -a
```

or pair it with `-l` for the long listing:

```
ls -la
```

***Protip:*** in Finder on Mac you can toggle hidden files with `Cmd + Shift + .`

### Wait, why are they hidden in the first place? (fun history)

Here's a "huh, neat" one: dotfiles being hidden was originally an **accident**. Early Unix `ls` wanted to skip the `.` and `..` entries (the current/parent directory shortcuts), so it just hid anything starting with a dot. People realized they could abuse that to hide clutter, and the whole convention was born. It's a happy bug, basically.

### Why are hidden files (and directories) important?

These are the contexts I've found them relevant in software engineering:

1) **Configuration**

Typically all of the software you install will have dotfiles to configure the application. For instance, I'm using the **mintty** terminal currently, and when I want to modify my settings or appearance, I edit my `.minttyrc` file 

***Also, people often call these dotfiles.***

2) **Environment Variables**

When you're working on a project involving git and you have API keys or other sensitive information you'd like to keep off the internet, you store that info in a `.env` file.

**BUT — and this is the important part — naming a file `.env` does NOT actually hide it from git.** Git tracks dotfiles just fine; the dot only hides them from *you* in the file listing. To actually keep `.env` from being pushed, you have to list it in a `.gitignore` file:

```
# .gitignore
.env
```

`.gitignore` is the file that tells git "ignore these, don't track them, don't push them." 

### Dotfiles you'll meet in the wild

Quick reference of the ones you might run into:  

```
.git/         the whole git repo lives here
.gitignore    what git should ignore
.env          your secrets / API keys
.bashrc       bash config (or .zshrc for zsh)
.ssh/         your ssh keys
.config/      catch-all config directory
```

