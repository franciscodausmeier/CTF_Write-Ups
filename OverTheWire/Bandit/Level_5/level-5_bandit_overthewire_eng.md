
# [Level 5](https://overthewire.org/wargames/bandit/bandit5.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Level 4 → Level 5

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/nivel-5_bandit_overthewire_esp.md)

> [PDF version.](https://drive.google.com/file/d/1fEu8YYAGmWnYbv_EjdmCvgQu81M1W6jw/view?usp=drive_link)

<br>

-----

<br>

## Challenge description.
> The password for the next level is stored in the only human-readable file in the inhere directory.\
Tip: if your terminal is messed up, try the “reset” command.

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit4 ".
- _password_: " 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ ".

<br>

> Commands you may need to solve this level.
- > [ls](https://man7.org/linux/man-pages/man1/ls.1.html),  [cd](https://man7.org/linux/man-pages/man1/cd.1p.html),  [cat](https://man7.org/linux/man-pages/man1/cat.1.html),  [file](https://man7.org/linux/man-pages/man1/file.1.html),  [du](https://man7.org/linux/man-pages/man1/du.1.html),  [find](https://man7.org/linux/man-pages/man1/find.1.html).

<br>

-----

<br>

## Procedure.

<br>

1. We use the [ls](https://man7.org/linux/man-pages/man1/ls.1.html) command to check for contents of the home folder.

<br>

```

	bandit4@bandit:~$ ls

```

<br>

---

<br>

2. After getting the location of the " inhere " directory with the previous command, we use the [ls](https://man7.org/linux/man-pages/man1/ls.1.html) command once to get to see all of the contents of that directory in detail.

<br>

```

	bandit4@bandit:~$ ls -lsah inhere/*

```

<br>

---

<br>

3. Once we get all of those files in the output of the previous command, we know that the flag of the level and password for the next, is in the content of one of the files in there, and that file is supposed to be of human readable.\
To search for those contents, we can use [file](https://man7.org/linux/man-pages/man1/file.1.html) to see if the encodings (or type) of each and every file tells us something about the type of contents these contain.

<br>

```

	bandit4@bandit:~$ file ./inhere/*

```

<br>

---

<br>

4. With the last command being executed, we get the type of all 10 files, and immediately, we notice that amongst them there´s one that has a type of encoding that makes it human readable, this file being " -file07 " and it´s type of encoding " ASCII text ". So we apply [cat](https://man7.org/linux/man-pages/man1/cat.1.html) to the file to print it´s contents.

<br>

```

	bandit4@bandit:~$ cat ./inhere/-file07

```

<br>

- And that should be it. The output of the last command shows us the flag of this level and the password for the next, " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>

---

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/level-5_bandit_overthewire.gif"/>
</p>

> Entire procedure.

<br>

---
