
> [Habilidades Generales](../README.md) | [PicoCTF](../../README.md) | [CTF's Write-Ups](../../../README.md)

# Obedient Cat

> <p> <span> Español - ESP </span> | <a href=https://github.com/frandausmeier/CTF_Write-Ups/blob/main/PicoCTF/General_Skills/Obedient_Cat/obedient-cat_general-skills_picoctf_eng.md> Inglés - ING<a/>. </p>

> [PDF version]().

---

<br>

- ## Descripción del challenge.
> Este archivo tiene la _flag_ a simple vista (o "in-the-clear"). [Descargar archivo](https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag).
>
> Dificultad: Facil\
> Tipo de _Challenge_: Habilidades Generales\
> Autor: SYREAL
  

<br>

## Información dada por el _challenge_.
- _Pista 1_.
    > Toda pista sobre ingresar un comando en terminal (como el siguiente), comienzan con "$"... todo lo que le sigue al signo de dolar deberá ser tipeado o copiado y pegado al terminal.

- _Pista 2_.
    > Para tener el archivo accesible en el _shell_, ingresá el siguiente comando al terminal: $ wget https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag.
  
- _Pista 3_.
    > $ man cat

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [man](https://man7.org/linux/man-pages/man1/man.1.html), [wget](https://man7.org/linux/man-pages/man1/wget.1.html), [cat](https://man7.org/linux/man-pages/man1/cat.1.html).
  
<br>
  
---
  
<br>

## Procedimiento.

<br>

1. Usamos el comando [ls](https://man7.org/linux/man-pages/man1/ls.1.html) para chequear los contenidos del directorio _home_.

<br>

```

	bandit4@bandit:~$ ls

```

<br>

---

<br>

2. Luego de ver los contenidos del directorio, empezamos a seguir la descripción del _challenge_. En eso es que descargamos con [wget](https://man7.org/linux/man-pages/man1/wget.1.html) el archivo de la descripción, como el link "Descargar archivo". Este comando es la segunda pista que el _challenge_ nos da en su descripción.

<br>

```

	bandit4@bandit:~$ wget https://mercury.picoctf.net/static/fb851c1858cc762bd4eed569013d7f00/flag

```

<br>

---

<br>

3. Luego de descargar el archivo, usamos [ls](https://man7.org/linux/man-pages/man1/ls.1.html) una vez mas para corroborar que el archivo nuevo que acabamos de descargar esté ahí 
  
<br>

```

	bandit4@bandit:~$ ls

```

<br>

---

<br>

4. Y ahí es donde lo encontramos, el archivo " flag ". Le aplicamos [cat](https://man7.org/linux/man-pages/man1/cat.1.html) en el terminal para revisar sus contenidos (comando que también es dado como pista en la descripción del _challenge_, en este caso la tercera), y ahí es donde encontramos la _flag_ del nivel.
  
<br>

```

	bandit4@bandit:~$ cat flag

```

<br>

- Y eso debería ser todo. El _output_ de este último comando nos muestra que el archivo " flag " es " picoCTF{s4n1ty_v3r1f13d_28e8376d} ".

<br>
  
---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/obedient-cat_general-skills_picoctf.gif"/>
</p>

> Procedimiento entero.

<br>

