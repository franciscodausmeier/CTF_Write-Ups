
# [Level 0](https://overthewire.org/wargames/bandit/bandit0.html) | [Bandit](https://overthewire.org/wargames/bandit/) | [OverTheWire](https://overthewire.org/wargames/)

> English | [Spanish](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_0/nivel-0_bandit_overthewire_esp.md) 

> [PDF version](https://github.com/frandausmeier/CTF_Write-Ups/blob/main/OverTheWire/Bandit/Level_0/level-0_bandit_overthewire_end.pdf).

-----

<br>

## Challenge description.

> "The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1".

<br>

## Information given by the challenge.

- **_hostname_**: " bandit.labs.overthewire.org ".
- **_port_**: " 22 " (2220).
- **_user_**: " bandit0 ".
- **_password_**: " bandit0 ".

<br>

> Commands you may need to solve this level.
- [ssh](https://manpages.ubuntu.com/manpages/noble/man1/ssh.1.html).

<br>

> Helpful reading material.
- [Secure Shell (SSH) on Wikipedia](https://en.wikipedia.org/wiki/Secure_Shell).
- [How to use SSH on wikiHow](https://www.wikihow.com/Use-SSH).


<br>


-----

<br>

## Procedure.

<br>

1. Use the key details given by the description of the challenge to fill the " SSH " command to log into the corresponding server for the challenge, following the structure of the SSH command:
			
<br>

```shell
	bandit0@bandit:~$ ssh user_name@host_name -p port_number
```

or

```shell
    bandit0@bandit:~$ ssh host_name -l user_name -p port_number
```

<br>

* where the "**-p**" option, allows us to specify the port for the login, and the number "**2220**" that indicates the default port (22) in the implementation of the SSH network protocol. The second example shows how we can use the option "**-l**" to specify the user name without having to use the _user_name@host_name_ notation.

<br>
			
```shell
	bandit0@bandit:~$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```

<br>

2. After correctly executing the command, you are going to be asked to enter the credentials given to you for the challenge to log into Level 1, being this the user "**bandit0**", and the password "**bandit0**", and that should be it.

<br>

-----

<br>

## Demonstration.

<br>

<p align="center">
  <img src="./attachments/level-0_bandit_overthewire.gif" />
</p>

<br>

----


