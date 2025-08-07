
# [Nivel 1](https://overthewire.org/wargames/bandit/bandit1.html) | [Bandit](https://github.com/frandausmeier/CTF_Write-Ups/tree/main/OverTheWire/Bandit) | [OverTheWire](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/README.es.md)

> Nivel 0 &rarr; Nivel 1.

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_1/level-1_bandit_overthewire_eng.md) 

> [Version en PDF.](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_1/nivel-1_bandit_overthewire_esp.pdf)

-----

<br>

## Descripción del _challenge_.
> Bandido Nivel 0 - Nivel 1

> Objetivo de nivel
> La contraseña para el siguiente nivel se almacena en un archivo llamado **readme** ubicado en el directorio de la casa. Utilice esta contraseña para registrarse en bandido1 usando SSH. Cada vez que encuentras una contraseña para un nivel, utilizar SSH (en el puerto 2220) para iniciar sesión en ese nivel y continuar el juego.

> Comandos que puede necesitar para resolver este nivel
> [ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html)

> **SUGERENCIA:** Crea un archivo para notas y contraseñas en tu máquina local.
> Las contraseñas para los niveles _no_ se guardan automáticamente. Si no los salvas tú mismo, tendrás que empezar de repasar desde bandido0.
> Las contraseñas también cambian ocasionalmente. Se recomienda tomar notas sobre cómo resolver cada desafío. A medida que los niveles se ponen más difíciles, las notas detalladas son útiles para volver a donde lo dejó, hacer referencia para problemas posteriores o ayudar a otros después de completar el desafío.

<br>

## Información dada por el _challenge_.
> Detalles útiles dados por el nivel anterior.
- _hostname_: " bandit.labs.overthewire.org ".
- _puerto_: " 22 " (2220).
- _usuario_: " bandit0 ".
- _contraseña_: " bandit0 ".

<br>

> Detalles nuevos dados por la descripción de este nivel.
- _comandos potencialmente útiles_: " ls, cd, cat, file, du, find ".

<br>

-----

<br>

## Procedimiento.

<br>

1. Una vez logeado en el nivel 0 (usando las credenciales usadas encontradas en el nivel anterior), usar los "comandos
que puedes llegar a necesitar para poder resolver en este nivel" encontrados en la descripción del _challenge_ para guiarse
en como resolver este nivel.

<br>

2. Entre los comandos encontrados en ese listado, podemos encontrar como particularmente útiles, los comandos "**ls**" y 
"**cat**". El primero, para poder listar todo el contenido de la ubicación específica en la cual nos
encontramos...

<br>

```shell
	bandit0@bandit:~$ ls
```

<br>

3. El siguiente comando siendo, " cat ", para poder leer los contenidos impresos en pantalla del archivo "readme" que llegamos a ver en el _output_ del comando anterior, siendo en este archivo donde se encuentra la solución de este nivel y la contraseña para poder logearse al nivel siguiente...

<br>

```shell
	bandit0@bandit:~$ cat readme
```

<br>

-----

<br>

## Adjunto.

<br>

<p align="center">
  <img src="./attachments/procedure_bandit1.png" />
</p>

<br>

-----

