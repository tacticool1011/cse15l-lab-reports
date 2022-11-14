# Lab Report 4 - Vim

## Part 1

In ``DocSearchServer.java``, change the name of the ``start`` parameter of ``getFiles``, and all of its uses, to instead be called ``base``.

1. ``/`` ``s`` ``t`` ``a`` ``r`` ``t``\
![Image](images/p1.png)
- - Jumps to an occurrence of ``start`` 

2. ``<Enter>``\
![Image](images/p2.png)
- - Jumps cursor to the start of the word and exits the command input

3. ``c`` ``e``\
![Image](images/p3.png)
- - Deletes the word and starts in insert mode

4. ``b`` ``a`` ``s`` ``e``\
![Image](images/p4.png)
- - Writes the word ``base``

5. ``<esc>``\
![Image](images/p5.png)
- - Exits insert mode

6. ``n``\
![Image](images/p6.png)
- - Goes to the next occurrence of ``start``

7. ``.``\
![Image](images/p7.png)
- - Repeats the previous command, which was ``c`` ``e`` and ``b`` ``a`` ``s`` ``e``

8. ``n``\
![Image](images/p10.png)
- -  Goes to the next occurrence of ``start``

9. ``.``\
![Image](images/p11.png)
- - Repeats the previous command, which was ``c`` ``e`` and ``b`` ``a`` ``s`` ``e``

10. ``:`` ``w`` ``q``\
![Image](images/p12.png)
- - Saves and exits vim.

## Part 2

### Style 1
- Style 1 took me ``89.05`` seconds. The difficulty was typing the correct scp parameters.

### Style 2
- Style 2 took me ``30.88`` seconds. There were actually no difficulties that came up when I was executing this style. Everything went smoothly.

### Reflection
- I would prefer ``Style 2`` over ``Style 1`` due to the fact that there is no file transfer needed. Typing the ``scp`` command parameter take so long because I need to make sure I am accessing it in the right folder and transferring it to the right folder.

- If I just need to make a minor change, I would probably just use vim on the remote computer because the effort to ``scp`` it is just not worth the time to type that command. However, if I am working on a huge chunk of code, I would probably work on it in ``Visual Studio Code`` because the editing environment is just better and the cost of time transfer it to the report to the time spent working on the actualy project is less than ``Style 1``.














