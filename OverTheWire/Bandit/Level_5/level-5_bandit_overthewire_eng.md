
# [Level 5](https://overthewire.org/wargames/bandit/bandit5.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Level 4 → Level 5

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/nivel-5_bandit_overthewire_esp.md)

> [PDF version.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/level-5_bandit_overthewire_eng.pdf)

-----

<br>

## Challenge description.
> The password for the next level is stored in the only human-readable file in the inhere directory.\ Tip: if your terminal is messed up, try the “reset” command.

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

1. ...

<br>

```
	bandit3@bandit:~$ ls
```
<br>

---

<br>

2. Use the _cd_ command to change our ubication into the " inhere " folder.

<br>

```
	bandit3@bandit:~$ cd inhere
```
<br>

---

<br>

3. We use the _ls_ command once again to check for the contents of the folder.

<br>

```
	bandit3@bandit:~$ ls
```
<br>

---

<br>

4. After looking for the file inside of the folder with the _ls_ command normally, we are going to realize that there are no files in that folder at first sight.\
What we can do from that position, is to check for the contents of that folder once again, with the _ls_ command, but adding it the `` -a `` option, to check for hidden files (or files that begin their name with a dot) at that location.

<br>

```
	bandit3@bandit:~$ ls -a
```
<br>

---

<br>

5. The output of that command shows us that the file was actually in that folder hidden. So we apply to it the _cat_ command to print the contents and obtain the password for the next level, this being " 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ ".

<br>

```
	bandit3@bandit:~$ cat ...Hiding-From-You
```

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
