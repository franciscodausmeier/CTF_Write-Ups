
# [Level 3](https://overthewire.org/wargames/bandit/bandit3.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/nivel-3_bandit_overthewire_esp.md)

> [PDF version.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/level-3_bandit_overthewire_eng.pdf)
-----

<br>

## Challenge description.
> Bandit Level 2 → Level 3

> Level Goal.
- > The password for the next level is stored in a file called  **spaces in this filename**  located in the home directory.

> Commands you may need to solve this level.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

> Helpful Reading Material.
- >  [Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename).

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit2 ".
- _password_: " 263JGJPfgU6LtdEvgfWU1XP5yac29mFx ".

<br>

> New useful information given by this level.
- _potentially useful commands_: " ls, cd, cat, file, du, find ".

<br>

-----

<br>

## Procedure.


<br>

1. Once again, after logging in to the current level with the credentials gained in the previous one, we use the **ls** command to see what we find at the file level at the beginning of this level.

<br>

```bash
	bandit2@bandit:~$ ls
```

<br>

- This command lets us know that we have a file in the home directory called " spaces in this filename ".

<br>

---

<br>

2. Among the commands recommended by the authors of the challenge, in addition to the **ls** and **cat** commands, we also find the **file** command, which allows us, among other uses, to corroborate the type of file we are dealing with, regardless of the extension that may appear in the file name. This is how we can use it to find out what type of file we are dealing with in this case.

<br>

```bash
	bandit2@bandit:~$ file spaces\ in\ this\ filename\
```
<br>

```bash
	bandit2@bandit:~$ file "spaces in this filename"
```

<br>

* Either one of these 2 options works fine to guarantee that the **file** command reads correctly the spaces in the name of the file.

<br> 

---

<br>

3. Having already used the **file** command and knowing that we are dealing with a text file, we know that we can use the **cat** command again to be able to print the contents of the file in the terminal.

<br>

```bash
	bandit2@bandit:~$ cat spaces\ in\ this\ filename\
```

<br>

```bash
	bandit2@bandit:~$ cat "spaces in this filename"
```

<br>

- Either one of these 2 options works fine to guarantee that the **cat** command reads correctly the spaces in the name of the file. And this is how we get the contents of the file printed on the screen and the password for the next level.

<br>

-----

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/level-3_bandit_overthewire.gif" />
</p>

<br>

----

