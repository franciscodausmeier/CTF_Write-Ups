
# [Nivel 5](https://overthewire.org/wargames/bandit/bandit5.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 4 → Nivel 5

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/level-5_bandit_overthewire_eng.md)

> [Versión en PDF.](https://drive.google.com/file/d/1MaBz3RZavlS8JlRKsIaRwNN8fXm1hgp1/view?usp=drive_link)

<br>

-----

<br>

## Descripción del _challenge_.
> La contraseña para el siguiente nivel está guardada en el único archivo humanamente leíble del directorio " inhere ".\
Tip: si tu terminal queda saturado, intenta con el comando _"reset"_.

<br>

## Información dada por el _challenge_.
> Detalles utiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puert_: " 22 " (2220).
- _usuario_: " bandit4 ".
- _contraseña_: " 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

-----

<br>

## Procedimiento.

<br>

1. Usamos [ls](https://man7.org/linux/man-pages/man1/ls.1.html) para revisar los contenidos de la carpeta _home_.

<br>

```
	
    bandit4@bandit:~$ ls

```

<br>

---

<br>

2. Luego de ubicar nuevamente el directorio " inhere " con el último comando, usamos [ls](https://man7.org/linux/man-pages/man1/ls.1.html) nuevamente para revisar todo lo que está dentro de esa carpeta.

<br>

```

	bandit4@bandit:~$ ls -lsah inhere/*

```

<br>

---

<br>

3. Una vez podamos ver todos los archivos dentro de " inhere " en el _output_ del comando anterior, siguiendo la descripción del _challenge_, sabemos que la _flag_ del nivel debería estar en el contenido de uno de estos.\
La pista que nos dió la descripción del _challenge_, es que la contraseña del siguiente nivel se encuentra en un archivo humanamente leíble dentro del directorio " inhere ". Siguiendo esto, lo que podemos hacer es aplicar el comando [file](https://man7.org/linux/man-pages/man1/file.1.html), que nos detalla tipos de archivo a todos los archivos dentro de esa carpeta para ver si alguno de ellos tiene alguna de las codificaciones que son humanamente leíbles.

<br>

```

	bandit4@bandit:~$ file ./inhere/*

```

<br>

---

<br>

4. Con el _output_ del último comando obtenemos el tipo de archivo de los 10 archivos en cuestión, e inmediatamente nos damos cuenta que entre ellos, hay 1 que tiene una codificación que indica que es un archivo humanamente leíble, siendo este " -file07 " y su codificación " ASCII text ", lo que indica que es un tipo de archivo de texto normal.
Sabiendo esto, probamos aplicarle [cat](https://man7.org/linux/man-pages/man1/cat.1.html) para ver si obtenemos la _flag_ en el _output_.

<br>

```

	bandit4@bandit:~$ cat ./inhere/-file07

```

<br>

- Y así adquirímos la _flag_ del nivel dentro del archivo " -file07 ", siengo el _output_ (y la _flag_) " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-5_bandit_overthewire.gif"/>
</p>

> Procedimiento entero.

<br>

