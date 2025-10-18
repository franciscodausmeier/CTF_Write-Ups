
# [Nivel 3](https://overthewire.org/wargames/bandit/bandit3.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 2 → Nivel 3

> Español | [English](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/level-3_bandit_overthewire_eng.md)

> [Versión en PDF.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/nivel-3_bandit_overthewire_esp.pdf)

-----

<br>

## Descripción del challenge.
> La contraseña para el siguiente nivel está guardada en un archivo llamado " --spaces in this filename-- ", ubicado en el directorio _home_.

<br>

## Información dada por el challenge.
> Detalles útiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit2 ".
- _contraseña_: " 263JGJPfgU6LtdEvgfWU1XP5yac29mFx ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

> Material de lectura útil.
- > [Búsqueda en Google de "spaces in filename"](https://www.google.com/search?q=spaces+in+filename).

<br>

-----

<br>

## Procedimiento.


<br>

1. Una vez mas, luego de habernos logeado al nivel actual (2) con las credenciales que obtuvimos en en el nivel previo, usamos el comando _ls_ para poder ver que encontramos inicialmente, en el directorio _home_ de este nivel.

<br>

```
	bandit2@bandit:~$ ls
```

<br>

- Es este comando el que nos hace saber que, precisamente en el directorio _home_, tenemos un archivo llamado " --spaces in this filename-- ".

<br>

2. Para poder imprimir los contenidos de este archivo en el terminal, podemos usar otra vez el comando _cat_, como hicimos con los archivos de niveles previos. El problema, puntualmente con este archivo, es que tiene multiples espacios incluidos (literalmente como caracteres) en el medio del nombre de este archivo, practica que no es del todo recomendable, ya que el terminal usualmente interpreta los espacios como una separación entre las distintas partes de un comando o como la separación entre multiples argumentos dentro de un comando, y no como otro caractér dentro del nombre del archivo.\
Para evadir esto, tenemos que modificar un poco la sintaxis del comando, especificando el nombre entero del archivo junto con su ruta relativa. En este caso, tenemos 2 maneras distintas de lograr esto. 

<br>

- Usar la barra inversa o invertida como caracter de quiebre en el comando, que indique el lugar del _string_ en donde se viene un caractér correspodiente a un espacio.

<br>

```
	bandit2@bandit:~$ file ./--spaces\ in\ this\ filename--
```
<br>

- o también usando apostrofes o comillas dobles como marcas al inicio y final del _string_ que hace al nombre del archivo.

<br>

```
	bandit2@bandit:~$ file './--spaces in this filename--'
```
> con el uso de apostrofes.

<br>

```
	bandit2@bandit:~$ file "./--spaces in this filename--"
```
> o usando comillas dobles.

<br>

* Cualquiera de estas 2 opciones funciona para garantizar que el comando _cat_ pueda leer correctamente los espacios en el nombre del archivo, y en consecuencia, el nombre del archivo en su enteridad como tal. Siguiendo cualquiera de estos 2 metodos es que podemos obtener los contenidos del archivo impresos en la pantalla de nuestro terminal, en este caso, la solución de este nivel (2) y la contraseña para logearnos al siguiente (3), siendo esta " MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx ".

<br> 

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-3_bandit_overthewire.gif>
</p>

<br>

----
