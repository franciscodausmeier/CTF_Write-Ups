
- - -

# [UnderTheWire.](https://underthewire.tech)

## [Century, Level 0](https://underthewire.tech/century)

- - - 

### Level 0 - Log with SSH.


#### ) Description of the challenge:

The goal of this level is to log into the game. Do the following in order to achieve this goal.
1. Obtain the initial credentials via the #StartHere channel on our Slack (link). Once you are in the channel, 
   scroll to the top to see the credentials.
2. After obtaining the credentials, connect to the server via SSH. You will need an SSH client such as Putty. 
   The host that you will be connecting to is century.underthewire.tech, on port 22.
3. When prompted, use the credentials for the applicable game found in the #StartHere Slack channel.
4. You have successfully connected to the game server when your path changes to “PS C:\Users\Century1\desktop>”.


#### ) Information given by the challenge:

- _host-name_: " **century.underthewire.tech** ".
- _port_: " **22** " (2220).
- _user_: " **century1** ".
- _password_: " **century1** ".

- - -

- - -

### Procedure.


1. Using the details given by the challenge, in this case, the _host-name_ and the _port_, to log effectively to the
   server of the challenge. In my case, I am going to be doing it with [PuTTY](https://www.putty.org/) as a SSH client.

   Look at the [first image attached](https://user-images.githubusercontent.com/71414554/244987878-2d552630-a873-4a11-a9b0-a19789eb556e.png) for this step.

- - -

2. Once you have entered those details to PuTTY, press "Open" in the application. That's where the login for the server is 
   going to get open and is going to ask you for a _user-name_ and _password_ that they are giving for this level on their 
   Slack channel ( " **century** " for _user-name_ and _password_ too).

   [Proof of this step](https://user-images.githubusercontent.com/71414554/244987890-0f2778ce-f323-4d24-aec9-d0162d186e65.png).

- - - 

3. And that should be it. Once you enter the correct credentials and it lets you in the server, you should see yourself in
   the directory " **PS C:\Users\Century1\desktop>** ", that is how you know you entered effectively to the Level 1.

   [Last step](https://user-images.githubusercontent.com/71414554/244987901-4138cd4d-8b5b-4299-af0e-70cd04db57f1.png) of the process.

- - -

### Attachments.


![captura1](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/2d552630-a873-4a11-a9b0-a19789eb556e)

![captura2](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/0f2778ce-f323-4d24-aec9-d0162d186e65)

![captura3](https://github.com/frandausmeier/CTF_Write-Ups/assets/71414554/4138cd4d-8b5b-4299-af0e-70cd04db57f1)


