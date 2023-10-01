### Objetivos 
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `ee388b88`

Additional details will be available after launching your challenge instance.

### Solución 
qshaix-picoctf@webshell:~$ ls -la
total 108
drwxr-xr-x 2 qshaix-picoctf qshaix-picoctf  4096 Sep 29 19:49 .
drwxr-xr-x 3 root           root              28 Sep 29 16:24 ..
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf  3771 Sep 29 16:24 .bashrc
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   807 Sep 29 16:24 .profile
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   167 Sep 29 16:25 .wget-hsts
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root            4443 Sep 29 19:40 README.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    34 Mar 16  2021 flag
qshaix-picoctf@webshell:~$ ssh ctf-player@venus.picoctf.net -p 58708
The authenticity of host '[venus.picoctf.net]:58708 ([3.131.124.143]:58708)' can't be estab
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
3ca613a1}
ctf-player@pico-chall$ cd ..
ctf-player@pico-chall$ ls
ctf-player
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ pwd
/
ctf-player@pico-chall$ ls
2of3.flag.txt  boot  etc   instructions-to-3of3.txt  lib64  mnt  proc  run   srv  tmp  var
bin            dev   home  lib                       media  opt  root  sbin  sys  usr
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ ls -la
total 92
drwxr-xr-x   1 root root 4096 Sep 29 20:00 .
drwxr-xr-x   1 root root 4096 Sep 29 20:00 ..
-rwxr-xr-x   1 root root    0 Sep 29 20:00 .dockerenv
-rw-r--r--   1 root root   17 Mar 16  2021 2of3.flag.txt
drwxr-xr-x   1 root root 4096 Mar 16  2021 bin
drwxr-xr-x   2 root root 4096 Apr 24  2018 boot
drwxr-xr-x   5 root root  340 Sep 29 20:00 dev
drwxr-xr-x   1 root root 4096 Sep 29 20:00 etc
drwxr-xr-x   1 root root 4096 Mar 16  2021 home
-rw-r--r--   1 root root   51 Mar 16  2021 instructions-to-3of3.txt
drwxr-xr-x   1 root root 4096 Mar 16  2021 lib
drwxr-xr-x   2 root root 4096 Feb 22  2021 lib64
drwxr-xr-x   2 root root 4096 Feb 22  2021 media
drwxr-xr-x   2 root root 4096 Feb 22  2021 mnt
drwxr-xr-x   1 root root 4096 Mar 16  2021 opt
dr-xr-xr-x 244 root root    0 Sep 29 20:00 proc
drwx------   2 root root 4096 Feb 22  2021 root
drwxr-xr-x   1 root root 4096 Sep 29 20:06 run
drwxr-xr-x   1 root root 4096 Mar 16  2021 sbin
drwxr-xr-x   2 root root 4096 Feb 22  2021 srv
dr-xr-xr-x  13 root root    0 Sep 29 20:00 sys
drwxrwxrwt   1 root root 4096 Mar 16  2021 tmp
drwxr-xr-x   1 root root 4096 Feb 22  2021 usr
drwxr-xr-x   1 root root 4096 Feb 22  2021 var
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls -la
total 32
drwxr-xr-x 1 ctf-player ctf-player 4096 Sep 29 20:06 .
drwxr-xr-x 1 root       root       4096 Mar 16  2021 ..
drwx------ 2 ctf-player ctf-player 4096 Sep 29 20:06 .cache
-rw-r--r-- 1 ctf-player ctf-player   80 Mar 16  2021 .profile
drw------- 1 ctf-player ctf-player 4096 Mar 16  2021 .ssh
-rw-r--r-- 1 ctf-player ctf-player   10 Mar 16  2021 3of3.flag.txt
drwxr-xr-x 1 ctf-player ctf-player 4096 Mar 16  2021 drop-in
ctf-player@pico-chall$  cat 3of3.flag.txt
3ca613a1}

picoCTF{xxsh_0ut_0f_\/\/4t3r_3ca613a1}
### Notas adicionales:



### Referencias:
