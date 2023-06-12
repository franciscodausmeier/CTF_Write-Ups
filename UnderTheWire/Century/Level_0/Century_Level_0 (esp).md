
- - - 

# [UnderTheWire.](https://underthewire.tech)

## Reporte/informe (Write-up) para [Century, Level 0](https://underthewire.tech/century).

- - -

### Nivel 0 - Logear con SSH con PuTTY.

#### ) Descripción del challenge:

El objetivo de este nivel es lograr logear dentro del primer nivel del _wargame_. Hacer lo siguiente
para poder lograr este objetivo:
1. Obtener las credenciales iniciales desde nuestro canal de Slack #StartHere. Una vez estés en el canal,
   hacer _scroll_ hasta la parte mas alta de este canal para poder ver las credenciales.
2. Luego de obtener las credenciales, conectar al server mediante el protocolo **SSH**. Para esto, vas a necesitar
   un cliente de **SSH** como PuTTy. El _host_ al que nos vamos a estar conectando es century.underthewire.tech, 
   y el puerto correspondiente es el 22.
3. Cuando se te pregunte por ellas, vas a tener que ingresar las credenciales encontradas en el canal #StartHere de
   Slack. 
4. Te vas a haber conectado efectivamente al _wargame_ una vez que el _path file_ del terminal cambia a 
   ``` PS C:\Users\Century1\desktop> ```.


#### ) Información dada por el _challenge_:

- _nombre-de-host_: " **century.underthewire.tech** ".
- _puerto_: " **22** " (2220).
- _nombre-de-usuario_: " **century1** ".
- _contraseña_: " **century1** ".

- - -

- - -

### Procedimiento.

1. Usando los detalles dados por el _challenge_, es este caso, el _nombre-de-host_ y el _puerto_, para poder logear de
   manera efectiva al servidor del _challenge_. En mi caso, voy a estar usando [PuTTY](https://www.putty.org/) como cliente 
   de **SSH**. 

   Dirigirse a la [primer imagen adjunta](https://user-images.githubusercontent.com/71414554/244987878-2d552630-a873-4a11-a9b0-a19789eb556e.png)
   para este paso.

- - -

2. Una vez que hayas ingresado los detalles en cuestión en PuTTY, presioná "Open" en la aplicación. Luego de esto, de estar correctamente otorgados
   el numero de puerto y el nombre del _host_, el servidor debería abrir y preguntar por las credenciales, preguntandonos por el _nombre-de-usuario_ 
   y la _contraseña_ que ellos nos dieron en el canal de Slack. 

   [Descripción gráfica de este paso](https://user-images.githubusercontent.com/71414554/244987890-0f2778ce-f323-4d24-aec9-d0162d186e65.png).

- - -

3. Esa debería ser la resolución al problema. Una vez se ingresen las credenciales de manera correcta y se te otorgue el
   ingreso al servidor, te deberías ver situado en el directorio ```PS C:\Users\Century1\desktop>```, así es como sabés con certeza
   que se te otorgó ingreso al servidor del nivel 1 de este _wargame_.

   [Ultimo paso](https://user-images.githubusercontent.com/71414554/244987901-4138cd4d-8b5b-4299-af0e-70cd04db57f1.png) del proceso.

- - -

### Archivos adjuntos.


![screenshot1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/2d552630-a873-4a11-a9b0-a19789eb556e)

![screenshot2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/0f2778ce-f323-4d24-aec9-d0162d186e65)

![screenshot3](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/4138cd4d-8b5b-4299-af0e-70cd04db57f1)

