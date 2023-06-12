
- - -

# [OverTheWire.](https://overthewire.org/wargames/)

## Reporte/informe (Write-up) para CTF [Bandit, nivel 0](https://overthewire.org/wargames/bandit/bandit0.html).

- - - 

### Nivel 0 - Logear con SSH.


#### ) Descripción del _challenge_: 

El objetivo de este _challenge_ es el poder aprender a logear dentro de los niveles del _wargame_ mediante **SSH**.
El _host_ al cual necesitás conectarte es " _bandit.labs.overthewire.org_ ", en el puerto 2220. El nombre de usuario 
con el cual hay que ingresar es " _bandit0_ " y la contraseña también es " _bandit0_ ". Una vez logeado al servidor, ir
a la pagina del Nivel 1 para conseguir como poder resolver el Nivel 1.


#### ) Información dada por el _challenge_:

- _nombre-de-host_: " **bandit.labs.overthewire.org** ".
- _puerto_: " **22** " (2220).
- _nombre-de-usuario_: " **bandit0** ".
- _contraseña_: " **bandit0** ".

- - -

- - -

### Procedimiento.


1. Usar los detalles dados por el _challenge_ para usar el comando " **SSH** " para logear al servidor correspondiente a este
   del challenge, siguiendo la siguiente estructura para el comando:

   ``` ssh nombre-de-usuario@nombre-de-host -p 2220 ```

   Donde la opción " **-p** " para el comando, nos permite clarificar el puerto correspondiente para lograr ingresar al servidor.

   ``` ssh bandit0@bandit.labs.overthewire.org -p 2220 ```

   [imagen](https://user-images.githubusercontent.com/71414554/244973917-0ccbdd21-38c6-435a-b2e0-25b007c6d231.png) de demostración de este paso.


- - -

2. Luego de haber ingresado de manera correcta el comando con cada una de sus partes, se te va a preguntar por la contraseña en cuestión
   (" **bandit0** ") y eso debería ser lo que te permita ingresar dentro del nivel 0 de este _challenge_. 
   Esta es la [imagen](https://user-images.githubusercontent.com/71414554/244973930-6f71eb9c-135d-49c2-adca-250e8517409f.png)
   de demostración de este último paso.

- - -

- - -


### Archivos adjunto.

![captura1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/0ccbdd21-38c6-435a-b2e0-25b007c6d231)
![captura2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/6f71eb9c-135d-49c2-adca-250e8517409f)


