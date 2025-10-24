
# [Nivel 7](https://overthewire.org/wargames/bandit/bandit7.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 7 → Level 8

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_7/nivel-7_bandit_overthewire_esp.md)

> [PDF version.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_7/level-7_bandit_overthewire_eng.pdf)

<br>

---

<br>

## Descripción del _challenge_.
> La contraseña para el siguiente nivel está guardada en algún lugar de este servidor y tiene todas estas características: \
\
	usuario bandit7 como dueño\
	bandit6 como grupo dueño\
	33 bytes de tamaño


<br>

## Información dada por el challenge.
> Detalles utiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit6 ".
- _contraseña_: " HWasnPhtq9AVKe0dmk45nxy20cvUa6EG ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

-----

<br>

## Procedimiento.

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

4. After the last use of the _ls_ command, we get as the output 20 different files named from " maybehere00 " to " maybehere19 ".\
So, knowing this, we start looking inside every single one of these folders looking for a non executable file, that has 1033 bytes of size.

<br>

```
	bandit4@bandit:~/inhere$ cd maybehere[..]
    
    bandit4@bandit:~/inhere/maybehere[..]$ ls -lsa
    
    bandit4@bandit:~/inhere/maybehere[..]$ cd ..
```

> These would be the commands we apply to each and every single folder looking for that file.

<br>

---

<br>

5. After looking individually in each folder, we reach " maybehere07 ", were we find a file called " .file2 " that is a non executable that also is 1033 bytes in size. So, we apply the _cat_ command to it, to see if it´s output is human readable, and these are the results.

<br>

```
	bandit4@bandit:~/inhere/maybehere07$ cat .file2
```

<br>

- And that´s where we find the human readable string that makes the _flag_ of this level, and the password for the next level. This being " HWasnPhtq9AVKe0dmk45nxy20cvUa6EG ".

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-7_bandit_overthewire.gif"/>
</p>

> Procedimiento entero.

<br>
