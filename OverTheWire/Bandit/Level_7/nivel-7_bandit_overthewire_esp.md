
# [Nivel 7](https://overthewire.org/wargames/bandit/bandit7.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 6 → Nivel 7

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_7/level-7_bandit_overthewire_eng.md).

> [Versión en PDF](https://drive.google.com/file/d/1reL17BBTmdpy3kNNtqpfW_T1FnhWNYoP/view?usp=drive_link).

<br>

---

<br>

## Descripción del challenge.
> La contraseña para el siguiente nivel está guardada en algún lugar del servidor y tiene las siguientes caracteristicas o propiedades: \
\
    bandit7 como usuario dueño del archivo\
    bandit6 como grupo dueño del archivo\
    33 bytes de tamaño
    

<br>

## Información dada por el challenge.
> Detalles utiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit6 ".
- _contraseña_: " HWasnPhtq9AVKe0dmk45nxy20cvUa6EG ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html),  [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html),  [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html),  [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html),  [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html),  [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html).

<br>

-----

<br>

## Procedimiento.

<br>

1. Nuevamente usamos _[ls](https://man7.org/linux/man-pages/man1/ls.1.html)_ para chequear los contenidos del directorio _home_, una vez nos logeamos.

<br>

```

	bandit4@bandit:~$ ls -lsah

```

<br>

---

<br>

2. Luego de haber usado _[ls](https://man7.org/linux/man-pages/man1/ls.1.html)_ nuevamente, buscando todos tipo de archivo en esa ubicación, nos damos cuenta de que no hay contenidos en la carpeta _home_ donde podamos buscar la _flag_ del _challenge_.\
Con esto en mente, deberíamos estar buscando en otras ubicaciones para poder encontrar el archivo donde la _flag_ puede estar guardada. Para este propósito, podemos usar otro de los comandos recomendados en la descripción del _challenge_, _[find](https://www.man7.org/linux/man-pages/man1/find.1.html)_. Con este comando, podemos usar multiples de las opciones que tiene para, junto a los datos dados en la descripción del _challenge_, poder ir guíando la busqueda del archivo en cuestión.

<br>

```

	bandit4@bandit:~$ file / type f ! -executable \
    > -size 33c -user bandit7 -group bandit6 \
    > 2>/dev/null

```

<br>

- Diseccionando este último comando, lo primero que hacemos es establecer el punto en donde queremos que comience la búsqueda, siendo este `` / ``, la carpeta _root_, dado que no tenemos ningún detalle sobre la posible ubicación del archivo en cuestión, vamos a tener que hacer la busqueda en todo el sistema.

<br>

- La sección `` type f ! -executable ``, donde `` f `` marca que estamos buscando un archivo de tipo regular (todo archivo que no sea un directorio o link simbólico) con el agregado de `` ! -executable ``, donde establecemos que estamos buscando un archivo no ejecutable, siendo `` ! `` la opción que marca que la siguiente función, `` -executable ``, es negativa.

<br>

- Por ultimo, también vamos a agregarle a ese comando `` 2>/dev/null `` como redireccionador de todos los mensajes de error de _output_ que podemos llegar a tener en el ejecutado del comando, refiriendose ese `` 2 `` todo mensaje de error como _standard output_, para enviar estos al archivo en la ubicación /dev/null y que no aparezcan en el terminal impresos junto al archivo que estamos buscando.

<br>

---

<br>

3. Una vez ejecutamos este ultimo comando, de estar bien redactado, deberíamos obtener el _output_ `` /var/lib/dpkg/info/bandit7.password ``, efectivamente dandonos como resultado el archivo en donde debería estar la _flag_ del nivel. Dicho esto, podemos imprimir los contenidos del archivo en el terminal normalmente, como lo venimos haciendo hasta este momento, usando _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_...

<br>

```

	bandit4@bandit:~$ cat /var/lib/dpkg/info/bandit7.password

```

<br>

- O, podemos usar otra de las opciones de _[find](https://www.man7.org/linux/man-pages/man1/find.1.html)_ como agregado al comando que nos dió la ubicación al archivo, siendo este, `` -exec ``.

<br>

```

	bandit4@bandit:~$ find / type f ! -executable \
    > -size 33c -user bandit7 -group bandit6 \
    > 2>/dev/null -exec cat {} +

```

<br>

- Agregando `` -exec ``, le estamos diciendo al terminal que redireccione el output del comando anterior (la ruta absoluta del archivo con la _flag_ del nivel, " bandit7.password ") hacia el comando _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_, donde los corchetes funcionan como _place holder_ o como espacio disponible para ese _output_, permitiendo ejecutar _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_ con el _output_ del último comando _[find](https://www.man7.org/linux/man-pages/man1/find.1.html)_ en una sola línea, haciendo la busqueda del archivo en primer lugar, y dando este como _input_ para la segunda parte del comando a partir de `` -exec ``, donde se va a imprimir en el terminal el contenido de los archivos, siendo estos " morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ". El caracter `` + `` al final del comando sirve únicamente como caracter de _break_ de este, dando lugar al final de este. 

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-7_bandit_overthewire.gif"/>
</p>

> Procedimiento entero.

<br>
