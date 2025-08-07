
# [Level 1](https://overthewire.org/wargames/bandit/bandit1.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Level 0 ``` &rarr ``` Level 1.


> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_1/nivel-1_bandit_overthewire_esp.md)

> [PDF version.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_1/level-1_bandit_overthewire_eng.pdf)
-----

<br>

## Challenge description.
> Bandit Level 0 → Level 1

> Level Goal
> The password for the next level is stored in a file called  **readme**  located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

> Commands you may need to solve this level
> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html)  ,  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html)  ,  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html)  ,  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html)  ,  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html)  ,  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

> **TIP:**  Create a file for notes and passwords on your local machine!
> Passwords for levels are  _not_  saved automatically. If you do not save them yourself, you will need to start over from bandit0.
> Passwords also occasionally change. It is recommended to take notes on how to solve each challenge. As levels get more challenging, detailed notes are useful to return to where you left off, reference for later problems, or help others after you’ve completed the challenge.

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit0 ".
- _password_: " bandit0 ".

<br>

> New useful information given by this level.
- _potentially useful commands_: " ls, cd, cat, file, du, find ".

<br>

-----

<br>

## Procedure.
1. Once logged in level 0 (using the credentials found in the previous level), look at the " Commands you may need to solve this level " given in the description of the challenge, and explore them to better guide yourself in solving the level.
    
<br>

2. Amongst all the commands that are on that list, there's a couple of them that are specially useful when it comes to reaching the flag in this level. The first one being " **ls** ", which allows you to list all the contents of the specific ubication in which you are in...

<br>

```
	bandit0@bandit:~$ ls
```

<br>

3. Then the second command, " **cat** ", used amongst other things, to simply print in the terminal the contents of a file. This is the command where are going to use to read the contents of the " readme " file that was found in the output of the last command, being this file where you find the solution to this challenge and the password to log into the next one...

<br>

```
	bandit0@bandit:~$ cat readme
```

<br>

-----

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/procedure_bandit1.png" />
</p>

<br>

----

