
# [Level 2](https://overthewire.org/wargames/bandit/bandit2.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/nivel-2_bandit_overthewire_eng.md)

> [PDF version.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/level-2_bandit_overthewire_eng.pdf)

-----

<br>

## Challenge description.

> Bandit Level 1 → Level 2.

> Level Goal.
- > The password for the next level is stored in a file called  **-**  located in the home directory.

<br>

> Commands you may need to solve this level.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

<br>

> Helpful Reading Material.
- > [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- > [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](https://linux.die.net/abs-guide/special-chars.html)

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit1 ".
- _password_: " ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If ".

<br>

> New useful information given by this level.
- _potentially useful commands_: " ls, cd, cat, file, du, find ".

<br>

-----

<br>

## Procedure.
1. Once logged in level 1 (using the credentials found in the previous level) and still looking and taking notice on the commands recommended by the author of the challenge, I start by once again using the **ls** command, to list all the contents. This lets us know, that there is a single file in the home directory called " - ".
    
<br>

```bash
	bandit1@bandit:~$ ls
```

<br>

2. In this case, to be able to see the contents of a file named like that, and using the **cat** command, you would have to specify the entire path to the file, being this " ./- ". You have to do this in order to avoid having the terminal interpreting that " - " as an indicator of " STDIN "  or " STDOUT ", or in other words, the file tree ubications of " div/stdin " and " div/stdout ". Specifying the entire path to the file should be enough to get as the output of the command all the contents of the file. 

<br>

```bash
	bandit1@bandit:~$ cat ./-
```

<br>

* and that is where you get in the content of the file the solution to the current level, the password to the level 2.

<br>

-----

<br>

## Attachment.

<br>

![procedure image 1](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/attachments/procedure_bandit2.png?raw=true)

<br>

----

