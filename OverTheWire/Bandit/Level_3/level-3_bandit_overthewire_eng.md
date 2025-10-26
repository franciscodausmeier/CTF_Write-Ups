
# [Level 3](https://overthewire.org/wargames/bandit/bandit3.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Level 2 → Level 3

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/nivel-3_bandit_overthewire_esp.md).

> [PDF version](https://drive.google.com/file/d/1L1JZP5ERuaf9Ij3QEZPDqsu0JkmSQxnx/view?usp=drive_link).

-----

<br>

## Challenge description.
> The password for the next level is stored in a file called " --spaces in this filename-- " located in the home directory.

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit2 ".
- _password_: " 263JGJPfgU6LtdEvgfWU1XP5yac29mFx ".

<br>

> Commands you may need to solve this level.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

> Helpful Reading Material.
- >  [Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename).

<br>

-----

<br>

## Procedure.

<br>

1. Once again, after logging in to the current level with the credentials gained in the previous one, we use the _ls_ command to see what we find at the file level at the beginning of this leve.

<br>

```

	bandit2@bandit:~$ ls

```

<br>

- This command lets us know that we have a file in the home directory called " spaces in this filename ".

<br>

2. To print the contents of the file in the terminal, we can use once again the command cat as we used in the file for the previous level. The problem with this one, is that it has multiple spaces
included (as actual characters) right in the middle of the name of the file. This is a problem because the terminal usually interprets spaces as a separation that establishes multiple arguments inside of a command, not as another character in the name of a file.\
To avoid this, we have to modify a little the syntax of the command in order to correctly specify the name of the file.In this case, we have 2 ways to achieve this.

<br>

- Using the backlslash as the breakcharacter that indicates where you have a space before this one actually appears...

<br>

```

	bandit2@bandit:~$ cat ./--spaces\ in\ this\ filename--

```

<br>

- or use either apostrophes or quotation marks at the start and end of the string chain that makes the name of the file.

<br>

```

	bandit2@bandit:~$ cat './--spaces in this filename--'

```
> with the use of apostrophes.

<br>

```

	bandit2@bandit:~$ cat "./--spaces in this filename--"

```
> or using quotation marks.

<br>

* Either one of these 2 options works fine to guarantee that the cat command reads correctly the spaces in the name of the file. And this is how we get the contents of the file printed on the screen and the password for the next level, this being " MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx ".

<br> 

---

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/level-3_bandit_overthewire.gif"/>
</p>

> Entire procedure.

<br>

----
