
# [Nivel 8](https://overthewire.org/wargames/bandit/bandit8.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 7 → Nivel 8

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_8/nivel-8_bandit_overthewire_esp.md).

> [Versión en PDF](https://drive.google.com/file/d/1CpFSQumI9F7E4xCMI6IeCH2iHqVhNU4o/view?usp=drive_link).

<br>

---

<br>

## Descripción del _challenge_.
> La contraseña del siguiente nivel está guardada en el archivo " data.txt " junto a la palabra " millionth ".

<br>

## Información dada por el _challenge_.
> Detalles utiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit7 ".
- _contraseña_: " morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [man](https://man7.org/linux/man-pages/man1/man.1.html),  [grep](https://man7.org/linux/man-pages/man1/grep.1.html),  [sort](https://www.man7.org/linux/man-pages/man1/sort.1.html),  [uniq](https://man7.org/linux/man-pages/man1/uniq.1.html),  [strings](https://www.man7.org/linux/man-pages/man1/strings.1.html),  [base64](https://man7.org/linux/man-pages/man1/base64.1.html), [tr](https://linux.die.net/man/1/tr), [tar](https://linux.die.net/man/1/tar), [gzip](https://linux.die.net/man/1/gzip), [bzip2](https://linux.die.net/man/1/bzip2), [xxd](https://linux.die.net/man/1/xxd).

<br>

-----

<br>

## Procedimiento.

<br>

1. We use the _[ls](https://man7.org/linux/man-pages/man1/ls.1.html)_ command to check for contents of the home folder, once we login.

<br>

```

	bandit4@bandit:~$ ls -lsah

```

<br>

---

<br>

2. After using the _ls_ command, looking for every type of file in that ubication, we realize that there are no contents in the _home_ folder where we can look for the flag of the level.\
With this in mind, we should be looking in other locations for the file with the flag. For that pourpose, we can use another of the recommended commands in the description of the challenge, _[find](https://www.man7.org/linux/man-pages/man1/find.1.html)_. With this command, we can use the options that it has to guide the search for the file with details that the challenge gave about the file.

<br>

```

	bandit4@bandit:~$ file / type f ! -executable \
    > -size 33c -user bandit7 -group bandit6 \
    > 2>/dev/null

```

<br>

- Ok, so quickly dissecting the last command, we establish the place where we want to start the search, `` / ``, this being root, given that we don´t have any details refering to where it might be, we are going to have to search in the entire system.

<br>

- The `` type f ! -executable `` section, where `` f `` establishes that we are looking for a regular file (every file that is not a directory or a symbolic link) with the added element of the `` ! -executable ``, where we establish that we are looking for a non executable file, with the `` ! `` acting as a negator for the `` -executable `` condition.

<br>

- And the other details. We establish the size of the file we are looking for with the option `` -size `` (`` 33c ``, for 33 bytes), `` -user `` to establish the user that owns the file (`` bandit7 ``), `` -group `` to tell the command the group owner of the command (`` bandit6 ``).

<br>

- At last, we are also going to add to the command `` 2>/dev/null ``, to redirect all of the standard output error messages, to the file _/dev/null_, a file that works as a data discard place in the entire system, specially for error messages, so these eventual error messages, specially for files that we don´t have read the read permissions, don't clog our terminal window and we only obtain the output we are interested in.

<br>

---

<br>

3. Once we execute that last command, if correctly written, we should be obtaining the output `` /var/lib/dpkg/info/bandit7.password ``, effectively confirming that we have obtained the location of the file with the flag. Now, we can print the output of this file normally, as we have been doing to this point, with the _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_ command...

<br>

```

	bandit4@bandit:~$ cat /var/lib/dpkg/info/bandit7.password

```

<br>

- Or, we can use another option of the _[find](https://www.man7.org/linux/man-pages/man1/find.1.html)_ command that allows us to redirect the output of a command into another, this being `` -exec ``.

<br>

```

	bandit4@bandit:~$ find / type f ! -executable \
    > -size 33c -user bandit7 -group bandit6 \
    > 2>/dev/null -exec cat {} +

```

<br>

- Adding `` -exec `` in here, we are telling the terminal to redirect the output of the command that gave us the supposed file that has the level of the flag, into the curly brackets that serve as a place holder for that output. So once in there, _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_ is going to be executed to that file in particular, giving us the output, this being " morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ". The `` + `` character is only acting as a break character for the command, indicating it's end.

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

