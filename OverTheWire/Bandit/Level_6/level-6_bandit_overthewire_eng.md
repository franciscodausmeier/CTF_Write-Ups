
# [Level 6](https://overthewire.org/wargames/bandit/bandit6.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Level 5 → Level 6

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_6/nivel-6_bandit_overthewire_esp.md)

> [PDF version.](https://drive.google.com/file/d/1fAYeduQDgqAkmDWB9T1-tHnYpbpLeBKh/view?usp=drive_link)

<br>

-----

<br>

## Challenge description.
> The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties: \
\
	human-readable\
	1033 bytes in size\
	not executable

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit5 ".
- _password_: " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>

> Commands you may need to solve this level.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

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

2. After getting the location of the " inhere " directory with the previous command, we use the [ls](https://man7.org/linux/man-pages/man1/ls.1.html) command to get to see all of the contents of that directory.

<br>

```

	bandit4@bandit:~$ ls -lsah inhere/

```

<br>

---

<br>

3. Once we get all of those files in the output of the previous command, we know that the flag of the level and password for the next, is in the context of one of the files in there.\
To search for those contents, we can use [find](https://man7.org/linux/man-pages/man1/find.1.html) to search files with the characteristics listed in the description of the challenge, as done in the next command... 

<br>

```

	bandit4@bandit:~$ find ./inhere/*\
    
    >> -type f ! -executable -size 1033cc

```

<br>

- First, we specify the location for the search with `` ./inhere/* ``, to search in the contents of anything that is inside of the inhere directory.\
Next, we specify the type of file and it´s condition as non executable with `` -type f ! -executable ``, and it´s size of 33 bytes with `` -size 1033c ``.

<br>

---

<br>

4. With the execution of that last command, we should be obtaining the exact file that has all of those characteristics, this being " -file07 ".\
As the last step for this level, we can just normally [cat](https://man7.org/linux/man-pages/man1/cat.1.html) that file to get the contents, which should have the password for the next level, or we can also use an adition to the command [find](https://man7.org/linux/man-pages/man1/find.1.html), this being `` -exec cat {} + ``. That `` -exec `` option, allows us to grab all the output of the previous part of the command (the exact location of the file with those characteristics) and put it inside the placeholders `` {} `` to execute a command on top of that output. In this case, the command being [cat](https://man7.org/linux/man-pages/man1/cat.1.html). That last `` + `` only works as a break character in this case, to indicate that the comand ends there. 

<br>

```

	bandit4@bandit:~$ find ./inhere/*\
    
    >> -type f ! -executable -size 1033cc -exec cat {} +

```

<br>

- And that should be it. The output of the last command shows us that the contents of the file " -file07 " have an output of " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>


---

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/level-6_bandit_overthewire.gif"/>
</p>

> Entire procedure.

<br>
