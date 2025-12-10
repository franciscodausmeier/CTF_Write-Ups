
> [General Skills Challenges](../README.md) | [PicoCTF](../../README.md) | [CTF's Write-Ups](../../../README.md)

# Obedient Cat

> <p> <span> English - ENG </span> | <a href=https://github.com/frandausmeier/CTF_Write-Ups/blob/main/PicoCTF/General_Skills/Obedient_Cat/obedient-cat_general-skills_picoctf_esp.md> Spanish - ESP<a/>. </p>

> [PDF version](https://drive.google.com/file/d/14AYVBPqjMA1vqLdR79M2UZ5eu6f-GL3f/view?usp=drive_link).

---

<br>

- ## Challenge description.
> This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag).
>
> Difficulty: Easy\
> Challenge Type: General Skills\
> Author: SYREAL
  

<br>

## Information given by the challenge.
- _Hint 1_.
  
	> Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.

- _Hint 2_.
	> To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag.

- _Hint 3_.
	> $ man cat

<br>

> Commands you may need to solve this level.
- > [man](https://man7.org/linux/man-pages/man1/man.1.html), [wget](https://man7.org/linux/man-pages/man1/wget.1.html), [cat](https://man7.org/linux/man-pages/man1/cat.1.html).
  
<br>
  
---
  
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

2. After seeing the contents in there, we start following the description of the challenge. In that, we download with [wget](https://man7.org/linux/man-pages/man1/wget.1.html), the file that we can find in the description by copying it's link in the " Download flag " part. This command it's the second hint that the description of the challenge gives us, that's where we find it.

<br>

```

	bandit4@bandit:~$ wget https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag

```

<br>

---

<br>

3. After downloading the file, we use [ls](https://man7.org/linux/man-pages/man1/ls.1.html) once again to check for a new file, and that's where we find the file that we downloaded, " flag ".

<br>

```

	bandit4@bandit:~$ ls

```

<br>

---

<br>

4. Knowing that the file is there, we use [cat](https://man7.org/linux/man-pages/man1/cat.1.html) to print it's contents in the terminal in search of the flag for the level. This command it's one of the clues that the challenge gives you (hint number 3).

<br>

```

	bandit4@bandit:~$ cat flag

```

<br>

- And that should be it. The output of the last command shows us that the file " flag " has an output of " picoCTF{s4n1ty_v3r1f13d_28e8376d} ".

<br>
  
---

<br>

## Attachment.

<br>

<p align="center">
  <img src="./attachments/obedient-cat_general-skills_picoctf.gif"/>
</p>

> Entire procedure.

<br>
