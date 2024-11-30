
# [Nivel 3](https://overthewire.org/wargames/bandit/bandit3.html) | [Bandit](https://github.com/frandausmeier/CTF_Write-Ups/tree/main/OverTheWire/Bandit) | [OverTheWire](https://overthewire.org/wargames/)

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/level-3_bandit_overthewire_eng.md) 

> [Version en PDF.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/nivel-3_bandit_overthewire_esp.pdf)

-----

<br>

## Descripción del _challenge_.
> Bandido Nivel 2 → 3

> Objetivo de nivel.
- > La contraseña para el siguiente nivel se almacena en un archivo llamado **espacios en este nombre** de **archivo** ubicado en el directorio de la casa.

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html), [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html), [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html), [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html), [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),[find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

> Material de lectura útil.
- > [Búsqueda de Google. Los espacios en el nombre de archivo.](https://www.google.com/search?q=spaces+in+filename)

<br>

## Información dada por el _challenge_.
> Detalles útiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit2 ".
- _contraseña_: " 263JGJPfgU6LtdEvgfWU1XP5yac29mFx ".

<br>

> Detalles nuevos dados por la descripción de este nivel.
- _comandos potencialmente útiles_: " ls, cd, cat, file, du, find ".

<br>

---
<br>


## Procedimiento.

<br>

1. Una vez mas, luego de logearnos al nivel actual con las credenciales ganadas en el nivel anterior, usamos el comando **ls** para poder ver con que nos encontramos a nivel de archivos en el comienzo de este nivel.

<br>

```bash
	bandit2@bandit:~$ ls
```

<br>

- Este comando nos hace saber que tenemos un archivo en el directorio _home_ llamado " spaces in this filename ".

<br>

---

<br>

2. Dentro de los comandos que nos recomendaron los autores del _challenge_, además de los comandos **ls** y  **cat**, nos encontramos también con el comando **file**, el cual nos permite, entre otros usos, el poder corroborar el tipo de archivo con el que estamos tratando, independientemente de la extensión que pueda figurar en el nombre del archivo. Así es como lo podemos usar para saber con que tipo de archivo estamos tratando en este caso.

<br>

```bash
	bandit2@bandit:~$ file spaces\ in\ this\ filename\
```

<br>

```bash
	bandit2@bandit:~$ file "spaces in this filename"
```

<br>

* Cualquiera de estas 2 opciones funcionan para leer correctamente los espacios del nombre del archivo en el contexto del comando **file**.

---

<br>

3. Ya habiendo usado el comando **file** y sabiendo que tratamos con un archivo de texto, sabemos que podemos usar nuevamente el comando **cat** para poder imprimir en terminal el contenido del archivo.

<br>

```bash
	bandit2@bandit:~$ cat spaces\ in\ this\ filename\
```

<br>

- Cualquiera de estas 2 opciones funcionan para leer correctamente los espacios del nombre del archivo en el contexto del comando **cat**. Y así es como obtenemos el contenido del archivo impreso en pantalla y la contraseña del siguiente nivel.

<br>

-----

<br>

## Adjunto.

<br>

![procedure image 1](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_3/attachments/procedure_bandit3.png?raw=true)

<br>

-----
