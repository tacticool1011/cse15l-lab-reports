# Lab Report 1 - Remote Access and the Filesystem

## Installing VScode

## Remotely Connecting
- Open command prompt by typing `cmd` in the windows search bar.
- Type ``ssh <username>@ieng6.ucsd.edu`` 
- Enter in your password when promoted (nothing will appear when you type so don't freak out)\
![Image](remote1.png)

## Trying Some Commands

## Moving Files with SCP
- Use this command to move files from the client to the remote computer\
``scp <filename> <username>@ieng6.ucsd.edu ``\
![Image](scp1.png)
- Accessing and running the file on the remote server using\
``cd <file location>``
``javac <filename>.java``\
``java <classname>``\
![Image](scp2.png)

## Setting an SSH Key
- ``ssh-keygen``
- Press enter with nothing entered for the prompts: \
``Enter file in which to save the key:``\
``Enter passphrase:``\
``Enter same passphrase again: ``
- SCP the public key (the file that ends in .pub) into the remote computer\
``scp /Users/andre/.ssh/id_rsa.pub <username>@ieng6.ucsd.edu:~/.ssh/authorized_keys``
- Now you should be able to login without entering your password\
![Image](ssh1.png)

## Optimizing Remote Running