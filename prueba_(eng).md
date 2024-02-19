
___

# [OverTheWire.](site.url)

## [Bandit, level 0](specific.challenge.url) CTF Write-up. [![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/frandausmeier/CTF_Write-Ups/blob/master/OverTheWire/Bandit/Level_0/Bandit_Level_0_(esp).md)

<br>

___

<br>

- ### Level 0 - [name.of.the.challenge] Log with SSH.
	- #### ) Description of the challenge:
		- [_description.of.the.challenge_]
	- #### ) Information given by the challenge:
		-   *hostname*: \" **bandit.labs.overthewire.org** \".
		-   *port*: \" **22** \" (2220).
		-   *user*: \" **bandit0** \".
		-   *password*: \" **bandit0** \".

<br>

___
___

<br>

- ### Procedure.
	- **1.**  Use the key details given by the description of the challenge to fill the \" **SSH** \" command to log into the corresponding server for the challenge, following the structure of the command:
		- **1.a.** `ssh user_name@host_name -p 2220`
			- where the " **-p**" option, allows for us to clarify the port for the login.
		- **1.b.** `ssh bandit0@bandit.labs.overthewire.org -p 2220`
			- ![screenshot_step1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/54930be3-99a4-4fd0-b27f-bb1feecd2324)

	- **2.**  After correctly entering the command, you are going to be asked to enter the password given to you for the challenge (\" bandit0 \"), and that should be it:
		-  ![screenshot_step2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/c531b3ab-136b-4d7c-afd9-338ad99b2644)

<br>

___
___

<br>

### Attachments.

![Step 1 (screenshot).](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/54930be3-99a4-4fd0-b27f-bb1feecd2324)

![Step 2 (screenshot).](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/c531b3ab-136b-4d7c-afd9-338ad99b2644)

<br>

___
