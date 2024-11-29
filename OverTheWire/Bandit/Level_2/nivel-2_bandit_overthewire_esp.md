
# [Nivel 2](https://overthewire.org/wargames/bandit/bandit2.html) | [Bandit](https://github.com/frandausmeier/CTF_Write-Ups/tree/main/OverTheWire/Bandit) | [OverTheWire](https://overthewire.org/wargames/)

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/level-2_bandit_overthewire_eng.md) 

> [Version en PDF.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/nivel-2_bandit_overthewire_esp.pdf)

-----

<br>

## Descripción del _challenge_.
> Bandido Nivel 1 - Nivel 2.

<br>

> Objetivo de nivel.
- > La contraseña para el siguiente nivel se almacena en un archivo llamado **-** ubicado en el directorio de la casa.

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

<br>

> Material de lectura útil.
- > [Búsqueda de nombre de archivo de la venta.](https://www.google.com/search?q=dashed+filename)
- > [Guía de Bash-scripting Avanzada - Capítulo 3 - Personajes especiales](https://linux.die.net/abs-guide/special-chars.html)

<br>

## Información dada por el _challenge_.
> Detalles útiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit1 ".
- _contraseña_: " ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If ".

<br>

> Detalles nuevos dados por la descripción de este nivel.
- _comandos potencialmente útiles_: " ls, cd, cat, file, du, find ".

<br>

-----

<br>

## Procedimiento.

<br>

1. Después de terminar de logearse al nivel 1, con la contraseña que obtuvimos en el _challenge_ anterior, y todavía
usando los comandos que nos están recomendando los autores del _challenge_, comenzamos utilizando otra vez el comando **ls**. Es este comando el que nos hace saber que hay un único archivo en la ubicación donde estamos, siendo este " - ".

<br>

```bash
	bandit1@bandit:~$ ls
```

<br>

2. En ese caso, y para evitar confusiones, para poder obtener o saber cual es el contenido de este archivo con el comando **cat**, deberíamos especificar el camino o _path_ completo al archivo, siendo este " ./- ", para evitar que el terminal tome a " - " como un argumento que indique " STDIN / STDOUT " o las ubicaciones " div/stdin " y " div/stdout " del sistema. Ya aclarado esto, usado el comando _cat_, eso debería darnos como _output_ el contenido del archivo, que es la solución de este nivel y la contraseña de ingreso al siguiente.

<br>

```bash
	bandit1@bandit:~$ cat ./-
```

<br>

-----

<br>

## Adjunto.

<br>

![procedure image 1](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/attachments/procedure_bandit2.png?raw=true)

<br>

-----

