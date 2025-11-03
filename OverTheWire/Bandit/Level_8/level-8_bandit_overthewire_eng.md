
# [Level 8](https://overthewire.org/wargames/bandit/bandit8.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Level 7 → Level 8

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_8/nivel-8_bandit_overthewire_esp.md).

> [PDF version](https://drive.google.com/file/d/13PI2El5tpnkFtrMERpxR5-CP4iYhQ0CE/view?usp=drive_link).

<br>

---

<br>

## Challenge description.
> The password for the next level is stored in the file data.txt next to the word millionth.

<br>

## Information given by the challenge.
> Useful information given by the previous level.
- _hostname_: " bandit.labs.overthewire.org ".
- _port_: " 22 " (2220).
- _user_: " bandit7 ".
- _password_: " morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ".

<br>

> Commands you may need to solve this level.
- > [man](https://man7.org/linux/man-pages/man1/man.1.html),  [grep](https://man7.org/linux/man-pages/man1/grep.1.html),  [sort](https://www.man7.org/linux/man-pages/man1/sort.1.html),  [uniq](https://man7.org/linux/man-pages/man1/uniq.1.html),  [strings](https://www.man7.org/linux/man-pages/man1/strings.1.html),  [base64](https://man7.org/linux/man-pages/man1/base64.1.html), [tr](https://linux.die.net/man/1/tr), [tar](https://linux.die.net/man/1/tar), [gzip](https://linux.die.net/man/1/gzip), [bzip2](https://linux.die.net/man/1/bzip2), [xxd](https://linux.die.net/man/1/xxd).

<br>

-----

<br>

## Procedure.

<br>

1. We use the _[ls](https://man7.org/linux/man-pages/man1/ls.1.html)_ command to check for contents of the home folder, once we login.

<br>

```

	bandit4@bandit:~$ ls -lsah

```

<br>

---

<br>

2. After using the _ls_ command, looking for every type of file in that ubication, we realize that the " data.txt " is in the home directory.\
Knowing this, we can take a peak at the contents of the file. We can do this once again, using _[cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html)_, or we can look at specific parts of the file with commands like _[head](https://man7.org/linux/man-pages/man1/head.1.html)_, that allows us to look at the first lines of a file, and _[tail](https://www.man7.org/linux/man-pages/man1/tail.1.html)_, for the last lines.

<br>

```

	bandit7@bandit:~$ head -n 5 data.txt

```

> To look at the first 5 lines of the file. The `` -n `` allows us to establish a specific number of lines we want to look at.

<br>

```

	bandit7@bandit:~$ tail -n 5 data.txt

```

> And this one, to look at the last 5 lines of the document. The `` -n `` option works exactly the same way it does with _[head](https://man7.org/linux/man-pages/man1/head.1.html)_.

<br>

---

<br>

3. _[Head](https://man7.org/linux/man-pages/man1/head.1.html)_ and _[tail](https://www.man7.org/linux/man-pages/man1/tail.1.html)_ shows us that the file has a good amount of contents, showing 5 full lines at the start and at the end of it. One thing that we can do to know the exact number of lines in a document (to know if it is convenient to use [cat](https://www.man7.org/linux/man-pages/man1/cat.1.html) to get the contents), is use [wc](https://man7.org/linux/man-pages/man1/wc.1.html), alongside it's `` -l `` option.

<br>

```

	bandit7@bandit:~$ wc -l data.txt

```

> [wc](https://man7.org/linux/man-pages/man1/wc.1.html) gives us the number of newlines, words and bytes of a document. `` -l `` is used to specify that we want the line count of the document.

<br>

---

<br>

4. As the output of the [wc](https://man7.org/linux/man-pages/man1/wc.1.html) we get that the " data.txt " has 98567 lines, so it's not going to be convenient to use _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_, unless we want to completely clog the terminal with 98 thousand lines of text.\
If we look at the recommended commands in the description of the challenge, one of the options can help us look amongst all of the lines on that document, the _[grep](https://www.man7.org/linux/man-pages/man1/grep.1.html)_ command. This command it's going to search for the string " millionth " inside of the document.

<br>

```

	bandit7@bandit:~$ grep -n millionth data.txt

```

> The command, as it stands, is going to look for and print the line that contains the string " millionth " in the document (search location) " data.txt ", giving us also the line number in which the string is located (that's the function of the  `` -n `` option in this case). 

<br>

- And with this last command, we finally get the line that has the flag of the level, to the right of the string " millionth ", just like the description of the challenge said, in the line 830 of the document.\
The flag of this level, and password for the next is " dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc ".

<br>

---

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/level-8_bandit_overthewire.gif"/>
</p>

> Entire procedure.

<br>
