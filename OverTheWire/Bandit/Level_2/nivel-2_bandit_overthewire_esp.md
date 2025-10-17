
# [Nivel 2](https://overthewire.org/wargames/bandit/bandit2.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Nivel 1 &rarr; Nivel 2.

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/level-2_bandit_overthewire_eng.md)

> [Versión en PDF.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_2/nivel-2_bandit_overthewire_esp.pdf)

-----

<br>

## Descripción del challenge.

> La contraseña para el siguiente nivel se encuentra en un archivo llamado " - " que se encuentra en el directorio _home_.

<br>

## Información dada por el challenge.
> Detalles útiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit1 ".
- _contraseña_: " ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html)  ,  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html)  ,  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html)  ,  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html)  ,  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html)  ,  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

<br>

> Material de lectura útil.
- [Búsqueda en Google de “dashed filename”](https://www.google.com/search?q=dashed+filename).
- [Guía de Bash-scripting Avanzado - Capítulo 3 - Caracteres Especiales](https://linux.die.net/abs-guide/special-chars.html).

<br>

-----

<br>

## Procedimiento.
1. Una vez en el nivel 1, empezamos usando el comando _ls_ para enlistar todos los contenidos. Esto nos deja ver que hay un archivo llamado " - " en el directorio _home_.

<br>
    
```
	bandit1@bandit~$ ls
```
 
<br>

2. En este caso, para poder ver los contenidos de un archivo con ese nombre, vamos a tener que especificar el _path_ entero hacia el archivo, siendo este " ./- " desde el directorio _home_. Uno tiene que hacer esto para poder evadir al terminal interpretando ese " - " como un indicador de " STDIN " o " STDOUT ", o como las versiones acortadas de las ubicaciones en el _file tree_ de " div/stdin " y " div/stdout " respectivamente. Especificando la ruta entera al archivo desde donde estamos debería ser suficiente para poder obtener los contenidos del archivo como _output_ utilizando el comando _cat_.

<br>

```
	bandit1@bandit:~$ cat ./-
```

<br>

- y así es como uno obtiene, en este caso, la solución al nivel actual, la contraseña de entrada o logeo al nivel 2, siendo esta " 
263JGJPfgU6LtdEvgfWU1XP5yac29mFx " como _output_ del ultimo comando.
<br>

-----

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-2_bandit_overthewire.gif" />
</p>

<br>

----

