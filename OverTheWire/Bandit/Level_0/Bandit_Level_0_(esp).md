___

# [OverTheWire.](sitio.url)

## Reporte/informe (Write-up) para CTF [Bandit, nivel 0](https://overthewire.org/wargames/bandit/bandit0.html). [![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/frandausmeier/CTF_Write-Ups/blob/master/OverTheWire/Bandit/Level_0/Bandit_Level_0_(eng).md)

<br>

- ### Nivel 0 - [nombre.del.challenge] Logearse con SSH.
	- #### ) Descripción del _challenge_:
		- [_descripción.del.challenge_]
	- #### ) Información que el _challenge_ otorga:
		-   *hostname*: \" **bandit.labs.overthewire.org** \".
		-   *port*: \" **22** \" (2220).
		-   *user*: \" **bandit0** \".
		-   *password*: \" **bandit0** \".

<br>

___
___

<br>

- ### Procedimiento.
	- **1.**  Usar los detalles dados por el _challenge_ para usar el comando " **SSH** " para logear al servidor correspondiente a este del _challenge_, siguiendo la siguiente estructura para el comando:
		- **1.a.** `ssh user_name@host_name -p 2220`
			- Donde la opción " **-p** " para el comando, nos permite clarificar el puerto correspondiente para lograr ingresar al servidor.
		- **1.b.** `ssh bandit0@bandit.labs.overthewire.org -p 2220`
			- ![screenshot_step1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/54930be3-99a4-4fd0-b27f-bb1feecd2324)
	- **2.**  2. Luego de haber ingresado de manera correcta el comando con cada una de sus partes, se te va a preguntar por la contraseña en cuestión (" **bandit0** ") y eso debería ser lo que te permita ingresar dentro del nivel 0 de este _challenge_. Esta es la [imagen](https://user-images.githubusercontent.com/71414554/244973930-6f71eb9c-135d-49c2-adca-250e8517409f.png) de demostración de este último paso.
		-  ![screenshot_step2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/c531b3ab-136b-4d7c-afd9-338ad99b2644)

<br>

___
___

<br>

- ### Archivos adjuntos.

	- ![Paso 1 (captura).](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/54930be3-99a4-4fd0-b27f-bb1feecd2324)
		
	- ![Paso 2 (captura).](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/c531b3ab-136b-4d7c-afd9-338ad99b2644)

<br>

___
