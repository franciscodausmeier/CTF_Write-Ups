
- - -

# [UnderTheWire.](https://underthewire.tech)

## [Century, Level 1](https://underthewire.tech/century) CTF Write-up. [![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/frandausmeier/CTF_Write-Ups/blob/master/UnderTheWire/Century/Level_1/Century_Level_1_(esp).md)

- - - 

### Level 1 - Found the password for Level 2.


#### ) Description of the challenge:

The password for Century2 is the build version of the instance of PowerShell installed on this system.

NOTE:
– The format is as follows: ```**.*.*****.****```
– Include all periods
– Be sure to look for build version and NOT PowerShell version

IMPORTANT:
Once you feel you have completed the Century1 challenge, start a new connection to the server, 
and log in with the username of Century2 and this password will be the answer from Century1. 
If successful, close out the Century1 connection and begin to solve the Century2 challenge. 
This concept is repeated over and over until you reach the end of the game.


#### ) Information given by the challenge:

- _host-name_: " **century.underthewire.tech** ".
- _port_: " **22** " (2220).

- - -

- - -

### Procedure.


1. Once you are logged to the first Level of the Century challenge (done in the [previous write-up](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/UnderTheWire/Century/Level_0/Century_Level_0%20(eng).md)),
   we can use the command ``` $PSVersionTable ``` to have the information specific to the engine version
   of the Powershell instance that we are running, which should give us the build version of the instance.

- - -

2. Looking at the output of the command we used on the previous step, we see that effectively, we obtained
   the version of the build, which should be, as indicated in the indications for this level, the password
   for the Level 2.

   _use of the command._
   [lugar-imagen-1]

- - - 

3. With that information, we disconnect from the server on the level, to try to connect to the server on the 
   level 2, with the user being the same as the .

- - -

### Attachments.


![screenshot1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/2d552630-a873-4a11-a9b0-a19789eb556e)

![screenshot2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/0f2778ce-f323-4d24-aec9-d0162d186e65)

![screenshot3](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/4138cd4d-8b5b-4299-af0e-70cd04db57f1)

