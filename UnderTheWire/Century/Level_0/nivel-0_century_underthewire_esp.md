
# [Nivel 1](https://underthewire.tech/century) | [Century](https://underthewire.tech/century) | [UnderTheWire](https://underthewire.tech/)
> Century Nivel 0 → Nivel 1

> Español | [Inglés](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/UnderTheWire/Century/Level_0/nivel-0_bandit_overthewire_esp.md).

> [Versión en PDF](https://drive.google.com/file/d/1W_3ptIVw4lfbCBa0bthvd6NzMW5QUeuZ/view?usp=drive_link).

<br>

---

<br>

## Descripción del _challenge_.
> The goal of this level is to log into the game. Do the following in order to achieve this goal.
> 1. Obtain the initial credentials via the #StartHere channel on our Slack (link). Once you are in the channel, scroll to the top to see the credentials.
> 2. After obtaining the credentials, connect to the server via SSH. You will need an SSH client such as Putty. The host that you will be connecting to is century.underthewire.tech, on port 22.
> 3. When prompted, use the credentials for the applicable game found in the #StartHere Slack channel.
> 4. You have successfully connected to the game server when your path changes to “PS C:\Users\Century1\desktop>”.

<br>

## Información dada por el _challenge_.
- _hostname_: " century.underthewire.tech ".
- _puerto_: " 22 " (2220).
- _usuario_: " century1 ".
- _contraseña_: " century1 ".

<br>

---

## Procedimiento.

<br>

1. Using the details given by the challenge, in this case, the host-name and the port, to log effectively to the server of the challenge. In my case, I am going to be doing it with [PuTTY](https://www.putty.org/) as a SSH client.

<br>

---

<br>

2. Una vez ingresamos los detalles a PuTTY, apretamos "Open" en la aplicación. Luego de esto, una vez abierto el terminal, ingresamos el _nombre-de-usuario_ y la _contraseña_ para poder logearnos (" century1 " tanto como usuario como contraseña). Estas se encuentran en el canal de Slack de UnderTheWire.

<br>

---

<br>

3. Y eso debería ser todo. Una vez entres al nivel 1 del _challenge_ con las credenciales correctas, al lado del _prompt_, deberías poder ver tu ubicación en la capeta ``` PS C:\Users\Century1\desktop> ```. 

<br>

---

<br>

### Adjunto.

<br>

<p align="center">
  <img src="./attachments/level-0_century_underthewire.gif"/>
</p>

> Procedimiento entero.

<br>

