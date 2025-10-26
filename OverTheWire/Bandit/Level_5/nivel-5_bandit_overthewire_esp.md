
# [Nivel 5](https://overthewire.org/wargames/bandit/bandit5.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 4 → Nivel 5

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_5/level-5_bandit_overthewire_eng.md)

> [Versión en PDF.](https://drive.google.com/file/d/1b3sVwl3pGwjXpkXYYbcyZA6oKkIeFQ2S/view?usp=drive_link)

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

1. Logeamos al nivel 4, y como primer medida, usamos el comando _ls_ para ver los contenidos del directorio _home_ de este nivel.

<br>

```
	
    bandit4@bandit:~$ ls

```

<br>

---

<br>

2. Luego de ubicar nuevamente el directorio " inhere " con el último comando, usamos _cd_ para cambiar nuestra ubicación dentro de dicha carpeta.

<br>

```

	bandit4@bandit:~$ cd inhere

```

<br>

---

<br>

3. Una vez dentro de " inhere ", volvemos a usar _ls_ otra vez para ver los contenidos del directorio.

<br>

```

	bandit4@bandit:~/inhere$ ls

```

<br>

---

<br>

4. A partir de este último uso del comando _ls_, nos damos cuenta que en esa ubicación hay 10 archivos de nombre similar que van desde el " -file00 " hasta " -file09 ".\
Sabiendo esto, usamos _cat_, y se lo aplicamos a todos los archivos, buscando precisamente entre ellos, el que tenga algún tipo de output que sea humanamente leíble. Según la descripción del _challenge_, ese debería ser el que contiene la _flag_.

<br>

```

	bandit4@bandit:~/inhere$ cat "./-file00"
    
    bandit4@bandit:~/inhere$ cat "./-file01"
    
    bandit4@bandit:~/inhere$ cat "./-file02"
    
    [...]
    
    bandit4@bandit:~/inhere$ cat "./-file07"
    
    bandit4@bandit:~/inhere$ cat "./-file08"
    
    bandit4@bandit:~/inhere$ cat "./-file09"

```

<br>

- El _output_ de todos los comandos usados en el paso anterior nos deja ver que el archivo que contiene la _flag_ es " -file07 ", siengo el _output_ (y la _flag_) " 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw ".

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src=".attachments/level-5_bandit_overthewire.gif"/>
</p>

> Procedimiento entero.

<br>

---
