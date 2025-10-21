
# [Level 5](https://overthewire.org/wargames/bandit/bandit5.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Level 4 → Level 5

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/nivel-5_bandit_overthewire_esp.md)

> [PDF version.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/level-5_bandit_overthewire_eng.pdf)

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
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

-----

<br>

## Procedure.

<br>

1. We use the _ls_ command to check for contents of the home folder.

<br>

```
	bandit4@bandit:~$ ls
```
<br>

---

<br>

2. After getting the location of the " inhere " directory with the previous command, we use the _cd_ command to change our ubication into that directory.

<br>

```
	bandit4@bandit:~$ cd inhere
```
<br>

---

<br>

3. Once inside " inhere ", we use the _ls_ command once again to check for the contents of the folder.

<br>

```
	bandit4@bandit:~/inhere$ ls
```
<br>

---

<br>

4. After the last use of the _ls_ command, we get as the output 10 different files named from " -file00" to "-file09".\
So, knowing this, we apply the _cat_ command to every single one of the files looking for the one that has human readable output in it, that should be the one that has the flag of the level according to the description of the challenge.

<br>

```
	bandit4@bandit:~/inhere$ cat "./-file00"
    
    bandit4@bandit:~/inhere$ cat "./-file01"
    
    bandit4@bandit:~/inhere$ cat "./-file02"
```
 
    [...]

    bandit4@bandit:~/inhere$ cat "./-file07"
    
    bandit4@bandit:~/inhere$ cat "./-file08"
    
    bandit4@bandit:~/inhere$ cat "./-file09"
```

<br>

- The output of those commands shows us that the file that has the flag is "-file07", with an output of " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>

---

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/level-5_bandit_overthewire.gif"/>
</p>

<br>

---
