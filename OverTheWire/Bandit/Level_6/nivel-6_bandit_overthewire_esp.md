
# [Nivel 6](https://overthewire.org/wargames/bandit/bandit6.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 5 → Level 6

> Español | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_6/level-6_bandit_overthewire_eng.md)

> [Versión en PDF.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_6/level-6_bandit_overthewire_eng.pdf)

<br>

-----

<br>

## Descripción del _challenge_.
> La contraseña para el siguiente nivel está guardada en un archivo en algún lugar en el directorio _inhere_ y tiene todas estas propiedades: \
\
	humanamente leíble\
	un tamaño de 1033 bytes\
	no ejecutable



<br>

## Información dada por el _challenge_.
> Detalles utiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit5 ".
- _contraseña_: " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

-----

<br>

## Procedure.

<br>

1. Logeamos al nivel 5, y como primer medida, usamos el comando _ls_ para ver los contenidos del directorio _home_ de este nivel.

<br>

```

	bandit4@bandit:~$ ls

```
<br>

---

<br>

2. Luego de ubicar nuevamente el directorio " inhere " con el último comando, usamos _cd_ para cambiar nuestra ubicación a ese directorio.

<br>

```

	bandit4@bandit:~$ cd inhere

```
<br>

---

<br>

3. Una vez dentro de " inhere ", usamos _ls_ otra vez, para revisar los contenidos del directorio.

<br>

```

	bandit4@bandit:~/inhere$ ls

```
<br>

---

<br>

4. Luego de ese último uso de _ls_, el _output_ nos da como resultado 20 archivos distintos llamados desde " maybehere00 " a " maybehere19 ".\
Con esto en mente, empezamos a buscar dentro de todas estas carpetas un archivo que sea no ejecutable, y que tenga 1033 bytes de tamaño.

<br>

```

	bandit4@bandit:~/inhere$ cd maybehere[..]
    
    bandit4@bandit:~/inhere/maybehere[..]$ ls -lsa
    
    bandit4@bandit:~/inhere$ cd ..

```

> Estos son los comandos que aplicamos en cada una de las carpetas en busqueda del archivo con la _flag_.

<br>

5. Luego de buscar individualmente in cada directorio, llegamos a " maybehere07 ", donde encontramos un archivo llamado " .file2 " que no es ejecutable y además tiene 1033 bytes de tamaño. Nuevamente, le aplicamos _cat_, para ver su si _output_ es leíble, y estos son los resultados.

<br>

```

	bandit4@bandit:~/inhere/maybehere07$ cat .file2

```

<br>

- Y así es como encontramos el archivo con el string que hace a la _flag_ del nivel y la contraseña del siguiente. Esta siendo " HWasnPhtq9AVKe0dmk45nxy20cvUa6EG ".

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-6_bandit_overthewire.gif"/>
</p>

> Entire procedure.

<br>
