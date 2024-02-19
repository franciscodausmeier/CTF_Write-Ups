
- - -

# [OverTheWire.](https://overthewire.org/wargames/)

## [Bandit, level 0](https://overthewire.org/wargames/bandit/bandit0.html) CTF Write-up. 

- - -
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/frandausmeier/CTF_Write-Ups/blob/master/OverTheWire/Bandit/Level_0/Bandit_Level_0 (eng).md)

[![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/frandausmeier/CTF_Write-Ups/blob/master/OverTheWire/Bandit/Level_0/Bandit_Level_0 (esp).md)
- - -

### Level 0 - Log with SSH.


#### ) Description of the challenge:

The goal of this level is for you to log into the game using SSH. 
The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. 
The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 
page to find out how to beat Level 1.


#### ) Information given by the challenge:

- _hostname_: " **bandit.labs.overthewire.org** ".
- _port_: " **22** " (2220).
- _user_: " **bandit0** ".
- _password_: " **bandit0** ".

- - -

- - -

### Procedure.


1. Use the key details given by the description of the challenge to fill the " **SSH** " command
   to log into the corresponding server for the challenge, following the structure of the command:

   ``` ssh user_name@host_name -p 2220 ```

   where the " **-p**" option, allows for us to clarify the port for the login.

   ``` ssh bandit0@bandit.labs.overthewire.org -p 2220 ``` 

   demonstration [image](https://user-images.githubusercontent.com/71414554/244929496-54930be3-99a4-4fd0-b27f-bb1feecd2324.png) about this step.

- - -

2. After correctly entering the command, you are going to be asked to enter the password given to
   you for the challenge (" bandit0 "), [and that should be it](https://user-images.githubusercontent.com/71414554/244928379-c531b3ab-136b-4d7c-afd9-338ad99b2644.png).

- - -

### Attachments.


![screenshoot1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/54930be3-99a4-4fd0-b27f-bb1feecd2324)

![screenshot2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/c531b3ab-136b-4d7c-afd9-338ad99b2644)
