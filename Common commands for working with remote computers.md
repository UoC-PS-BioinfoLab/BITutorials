# Common commands for working with remote computers



## Moving files/folders to and from remote



### Using VSCode/MobaXterm

The process should be a straightforward matter of right-clicking the file/folder you want and selecting *download* 

### Using the terminal

The command to use is *scp*. It has the following structure:

```bash
scp [SOURCE] [TARGET]
```

**scp** stands for **S**ecure **C**o**p**y, which is a protocol that allows you to copy files between two computers over a network.

When specifying the location in the remote computer, you use the format `[user]@[ip]:~/`. A few things to note here:

- The colon (:) symbol in between the ip address and the tilde symbol. Used to separate the computer ID on the network, from the path in the computer you're interested in.
- The tilde (~) symbol, which is used to denote your path is starting from your user home folder in the Linux system

