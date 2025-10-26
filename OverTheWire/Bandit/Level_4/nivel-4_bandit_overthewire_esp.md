
# [Nivel 4](https://overthewire.org/wargames/bandit/bandit4.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 3 → Nivel 4

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_4/level-4_bandit_overthewire_eng.md).

> [Versión en PDF](https://drive.google.com/file/d/1ZJ45JXEeEoTxAQA40-v-m3E5dbzkxQa2/view?usp=drive_link).

<br>

-----

<br>

## Descripción del challenge.
> La contraseña para el siguiente nivel se encuentra guardada en un archivo escondido en el directorio " inhere ".

<br>

## Información dada por el challenge.
> Detalles útiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit3 ".
- _contraseña_: " MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx ".

<br>

> Comandos que puede necesitar para resolver este nivel.

- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

-----

<br>

## Procedimiento.

<br>

1. Para comenzar, volvemos a usar el comando _ls_ para poder ver los contenidos de la carpeta _home_ del usuario en el que estamos. Esto nos muestra la localización del directorio " inhere ", el cual tiene el archivo con la _flag_ de este nivel, según la descripción del _challenge_.

<br>

```
	
    bandit3@bandit:~$ ls

```

<br>

---

<br>

2. Usar el comando _cd_ para cambiar nuestra ubicación dentro del directorio " inhere ".

<br>

```

	bandit3@bandit:~$ cd inhere

```

<br>

---

<br>

3. Ya dentro del directorio, hacemos uso del comando _ls_ otra vez para buscar en el contenido del directorio el archivo con el _flag_ del _challenge_.

<br>

```

	bandit3@bandit:~/inhere$ ls

```

<br>

---

<br>

4. Luego de chequear los contenidos de esta carpeta con el comando _ls_, nos vamos a dar cuenta de que no hay archivos ahí a simple vista.\
Lo que podemos hacer desde esta posición, es controlar por archivos ocultos dentro de esta carpeta, otra vez, usando el comando _ls_, con el agregado de la opción `` -a `` para poder corroborar por archivos ocultos (o archivos que comienzen su nombre con un punto).

<br>

```

	bandit3@bandit:~/inhere$ ls -a

```

<br>

---

<br>

5. El _output_ del comando nos muestra que el archivo efectivamente está en ese directorio pero oculto. Así que le aplicamos el comando _cat_ para imprimir sus contenidos en el terminal y obtener la contraseña para el siguiente nivel, siendo esta " 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ ".

<br>

```

	bandit3@bandit:~/inhere$ cat ...Hiding-From-You

```

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-4_bandit_overthewire.gif"/>
</p>

> Procedimiento entero.

<br>

---
