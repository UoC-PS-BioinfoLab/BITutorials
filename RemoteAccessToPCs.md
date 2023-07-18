# Getting into PCs remotely



# SSH

**SSH** stands for **S**ecure **Sh**ell, which is a protocol through which you can open a shell (also known as a *terminal* window) inside a computer, from another computer in the network. 

This is beneficial because that means you can use the resources of a computer without having to be right next to it all the time. And you can check the progress of a machine doing a job the same way. 

A shell is the name given to a terminal/Powershell window in your OS. So you can think of this as *remotely* opening a Powershell window in another computer from somewhere else in the network to do work. If you want to learn more, feel free to google it. There are plenty of good resources that can help you learn. Here I will only be showing how you can use it when connecting to PCs in a network.

## Using SSH via terminal/powershell 

The ssh program should be available on all basic Linux distributions by default and it is now also integrated as part of Windows Powershell on windows 10 and 11. 

> If you want to test whether your OS has ssh, then just open your terminal (or Powershell on Windows) and type 'ssh'. If it is present in the terminal, you will get an output that shows the usage of ssh.

The general command for using ssh to connect is in the form: 

```shell
ssh [username]@[ip_address]
```

For example: 

```shell
ssh janith@10.21.8.152
```

#### A couple of things to remember here:

- You must have a user account in the computer you're connecting to in order to ssh into it
- You must know the IP address of the computer you want to connect to
  - If you want to find the IP of a computer the commands are:
    - `ipconfig` on a powershell/cmd for windows
    - `ip -4 address` for Linux
  - And then find the IPv4 address under ethernet/wi-fi adapters
  - The address should take the form of 4 numbers connected by '.'s
    - *e.g:* The IP address for the HPC is 10.21.8.150, most home wi-fi networks have addresses in the range of 192.168.x.x



If you typed the command properly, the program will connect and ask you if you want to trust the computer you're connecting to. Since the computers you'll usually be connecting to are safe, type `yes`. 

Then you will be prompted for a password. This is the user password for the user you created on that computer. 

After typing it in, you should now have opened a shell in the remote computer. You will know it succeeded by having your current shell have the [Username]@[PC_name] form.

## Using SSH via VSCode

## Using SSH via MobaXterm



## Using ssh keys to avoid having to type passwords all the time

### ssh-keygen

### The order to do things

#### 1. Creating a key pair

#### 2. Adding your public key to the authorized keys on remote

#### 3. Configuring your sshconfig to use the private key when joining





