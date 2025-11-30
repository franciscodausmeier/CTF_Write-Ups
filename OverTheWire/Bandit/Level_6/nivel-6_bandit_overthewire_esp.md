
# [Nivel 6](https://overthewire.org/wargames/bandit/bandit6.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 5 → Nivel 6

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_6/level-6_bandit_overthewire_eng.md).

> [Versión en PDF](https://drive.google.com/file/d/13BhnJk-vFQgefTedmwjARIP1ys4ij1GB/view?usp=drive_link).

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

## Procedimiento.

<br>

1. Usamos [ls](https://man7.org/linux/man-pages/man1/ls.1.html) para revisar los contenidos del directorio _home_.

<br>

```

	bandit4@bandit:~$ ls

```
<br>

---

<br>

2. Luego de ubicar nuevamente el directorio " inhere " con el último comando, usamos [ls](https://man7.org/linux/man-pages/man1/ls.1.html) nuevamente para revisar todos los contenidos del directorio en detalle.

<br>

```

	bandit4@bandit:~$ ls -lsah inhere/

```
<br>

---

<br>

3. Una vez obtenemos el _output_ del último comando, nos damos cuenta que el archivo con la _flag_ del nivel tiene que estar dentro de uno de esos directorios del _output_.\
Para buscar esos contenidos, podemos usar el comando [find](https://man7.org/linux/man-pages/man1/find.1.html) para buscar archivos con las características detalladas en la descripción del _challenge_ de manera recursiva desde " inhere ".

<br>

```

	bandit4@bandit:~$ find ./inhere/*\
    
    >> -type f ! -executable -size 1033c

```

<br>

- En primera instancia, detallamos la ubicación desde la cual parte la búsqueda con `` ./inhere/* ``, precisamente para buscar entre los contenidos de todo lo que haya en el directorio " inhere ".\
Luego de eso, especificamos el tipo de archivo que estamos buscando y su condición como no ejecutable con `` -type f ! -executable ``, y finalmente, su tamaño de 33 _bytes_ con `` -size 1033c ``. 

<br>

---

<br>

4. Con la ejecución de ese último comando, deberíamos estar obteniendo la ubicación exacta del archivo o los archivos que reunan las características detalladas en el comando. En este caso, el archivo obtenido en el _output_ del comando es " .file2 " y su ruta desde _home_ es `` ./inhere/maybehere07/.file2 ``

<br>

- Sabiendo el archivo, como último paso del procedimiento podemos usar normalmente [cat](https://man7.org/linux/man-pages/man1/cat.1.html) el archivo para obtener el _output_ como lo venimos haciendo en niveles anteriores, o podemos hacerle un agregado al comando [find](https://man7.org/linux/man-pages/man1/find.1.html), este siendo `` -exec cat {} + ``. La opción `` -exec `` nos posibilita poder tomar el _output_ de un comando y posicionar este _output_ entre las llaves, que en el caso de este comando sirven como _placeholders_ para tener el _output_ ubicado y poder aplicarle un segundo comando, en este caso y con esta sintaxís sería [cat](https://man7.org/linux/man-pages/man1/cat.1.html).\
El último caractér, `` + `` en este caso, solamente sirve como _breakcharacter_ para el comando, marcando el fin de este.

<br>

```

	bandit4@bandit:~$ find ./inhere/*\
    
    >> -type f ! -executable -size 1033c -exec cat {} +

```

<br>

- Y eso debería ser todo. El contenido de el archivo " .file2 " es " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

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
