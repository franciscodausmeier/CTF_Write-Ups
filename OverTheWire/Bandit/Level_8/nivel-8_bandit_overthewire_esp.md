
# [Nivel 8](https://overthewire.org/wargames/bandit/bandit8.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)
> Bandit Nivel 7 → Nivel 8

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_8/level-8_bandit_overthewire_eng.md).

> [Versión en PDF](https://drive.google.com/file/d/1YVij6wmYISmL3I8H83_qHRZx9ZfsfFVx/view?usp=drive_link).

<br>

---

<br>

## Descripción del _challenge_.
> La contraseña del siguiente nivel está guardada en el archivo " data.txt " junto a la palabra " millionth ".

<br>

## Información dada por el _challenge_.
> Detalles utiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit7 ".
- _contraseña_: " morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj ".

<br>

> Comandos que puede necesitar para resolver este nivel.
- > [man](https://man7.org/linux/man-pages/man1/man.1.html),  [grep](https://man7.org/linux/man-pages/man1/grep.1.html),  [sort](https://www.man7.org/linux/man-pages/man1/sort.1.html),  [uniq](https://man7.org/linux/man-pages/man1/uniq.1.html),  [strings](https://www.man7.org/linux/man-pages/man1/strings.1.html),  [base64](https://man7.org/linux/man-pages/man1/base64.1.html), [tr](https://linux.die.net/man/1/tr), [tar](https://linux.die.net/man/1/tar), [gzip](https://linux.die.net/man/1/gzip), [bzip2](https://linux.die.net/man/1/bzip2), [xxd](https://linux.die.net/man/1/xxd).

<br>

-----

<br>

## Procedimiento.

<br>

1. Usamos _[ls](https://man7.org/linux/man-pages/man1/ls.1.html)_ nuevamente para chequear los contenidos del directorio _home_ una vez nos logeamos.

<br>

```

	bandit4@bandit:~$ ls -lsah

```

<br>

---

<br>

2. Ya habiendo usado _[ls](https://man7.org/linux/man-pages/man1/ls.1.html)_, buscando cualquier tipo de archivo en el proceso, nos damos cuenta que el archivo " data.txt " del que habla la descripción del _challenge_ está en esa ubicación.\
Sabiendo esto, podemos ver de a poco los contenidos del archivo. Podemos hacer esto volviendo a usar _[cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html)_, o podemos probar mirando partes específicas de los contenidos del documento usando comandos como _[head](https://man7.org/linux/man-pages/man1/head.1.html)_, con el cual podemos ver las primeras lineas de un documento, y _[tail](https://www.man7.org/linux/man-pages/man1/tail.1.html)_, que nos permite revisar las ultimas lineas de un archivo.

<br>

```

	bandit7@bandit:~$ head -n 5 data.txt

```

> Mirando las 5 primeras lineas del archivo. La opción `` -n `` nos permite establecer un numero específico de lineas que queremos revisar, en este caso 5.

<br>

```

	bandit7@bandit:~$ tail -n 5 data.txt

```

> Y este otro, para mirar a las ultimas 5 lineas del documento. La opción `` -n `` funciona exactamente de la misma manera para este comando que con  _[head](https://man7.org/linux/man-pages/man1/head.1.html)_.

<br>

---

<br>

3. _[Head](https://man7.org/linux/man-pages/man1/head.1.html)_ y _[tail](https://www.man7.org/linux/man-pages/man1/tail.1.html)_ nos deja ver que el archivo tiene una buena cantidad de contenidos y que no tenemos certeza de la cantidad de líneas que este puede llegar a tener. Algo mas que podemos hacer para saber el numero exacto de líneas en los contenidos de un documento (para saber si es conveniente usar [cat](https://www.man7.org/linux/man-pages/man1/cat.1.html) para imprimir en pantalla todos los contenidos), es usar [wc](https://man7.org/linux/man-pages/man1/wc.1.html), junto a su opción `` -l ``.

<br>

```

	bandit7@bandit:~$ wc -l data.txt

```

> [Wc](https://man7.org/linux/man-pages/man1/wc.1.html) nos da el numero de lineas, palabras o bytes de un documento. La opción `` -l `` se usa para especificar que el output que queremos es el numero de lineas del documento.

<br>

---

<br>

4. Dentro del _output_ de [wc](https://man7.org/linux/man-pages/man1/wc.1.html), obtenemos 98567 como el numero de lineas dentro del archivo " data.txt ", por lo cual, sabemos que no va a ser conveniente usar _[cat](https://www.man7.org/linux/man-pages/man1/cat.1.html)_, ya que con ese numero del lineas, nos puede congestionar muy facilmente el terminal con muchísmo _output_ que no nos interesa.\
Si miramos dentro de los comandos recomendados por la descripción del _challenge_, una de las opciones nos puede ayudar a buscar entre los contenidos de " data.txt ", el comando _[grep](https://www.man7.org/linux/man-pages/man1/grep.1.html)_. Este comando nos va a posibilitar usar el _string_ " millionth " que nos dió la descripción del challenge, como el termino que está justo al lado de la _flag_ del nivel.

<br>

```

	bandit7@bandit:~$ grep -n millionth data.txt

```

> El comando, como está escrito, va a buscar e imprimir en pantalla la o las líneas que contienen el _string_ " millionth " dentro del documento " data.txt ", dandonos también el numero de línea en la cual el _string_ se encuentra localizado (esa es la función de la opción `` -n `` en este caso).

<br>

- Y con este último comando, finalmente obtenemos la línea que tiene el _flag_ del nivel, justo a la derecha del _string_ " millionth ", como la descripción del _challenge_ nos aclaró, en la linea 830 de " data.txt ".\
La _flag_ de este nivel y contraseña del siguiente es " dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc ".

<br>

---

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-8_bandit_overthewire.gif"/>
</p>

> Procedimiento entero.

<br>

