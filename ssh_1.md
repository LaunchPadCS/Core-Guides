## SSH Basics

The `ssh` program is one of the most important skills to learn for working on a terminal. This program allows you to connect to another machine and execute terminal commands from there.

### How to SSH
The syntax for ssh is easy to learn. You just need to know your username and the address of the server you want to connect to:  

```terminal
ssh <myusername>@servername.com
```

If you're a Purdue student, you can connect to `data`, which is the name of our main CS server. If your purdue username is `jdoe`, then you would connect to the purdue server by running this command:

```terminal
ssh jdoe@data.cs.purdue.edu
```

Once you're connected to the server, you can run run commands just like you do on your personal computer. To exit the ssh session and return to your own device, just type `exit`.


### Key-based Authentication
By default, many servers will ask you to type in your password if you try to connect. However, a more secure method is to use `public and private keys`  to prove your identity.  The way this system works is a little complicated, but the basic idea is that you can prove your identity without having to type in a secret password. Some servers will even be set up so that you need to authenticate this way instead of using a password.

#### Generate a Key Pair on your machine
If you want to set this up, check your computer to see if you already have a public/private key pair. They're usually in `~/.ssh/` on mac/linux (or `C:\Users\MyUsername\.ssh/` on Windows).  

If you don't see any files in that folder, you need to generate a keypair. To do that, run `ssh-keygen`  and don't enter a password if you're asked. This program will create an `id_rsa` and `id_rsa.pub` file in the correct folder.

The `id_rsa`  file is your *private key*, and it should not be shared with anybody or typed in anywhere. On the other hand, the `id_rsa.pub`file is your *public key*, and it's totally safe to share that with anybody.  If you open the `id_rsa.pub` file, it should look like a bunch of garbage text followed by your name or email address.  

#### Set up the server to accept your key
Once you have a key pair, you can add your public key to the server. Copy the contents of the `id_rsa.pub` file from your laptop and then ssh into the machine you want to set up.

Find the file called `authorized_keys` in the `~/.ssh/` folder. If the folder or file doesn't exist already, you can create it yourself (`mkdir ~/.ssh` and then `touch ~/.ssh/authorized_keys`). Finally, paste your public key into this file and save.

Once this is set up correctly, the server will let you log in without entering a password. This is super nice because it saves time, but it's also a lot more secure. With this method, you don't need to send your password or any sensitive information over the internet.  
