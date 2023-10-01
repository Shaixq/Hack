## Objetivos
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/a5683698ac318b47bd060cb786859f23/flag).
## Solucion
qshaix-picoctf@webshell:~$ ls -la
total 40
drwxr-xr-x 2 qshaix-picoctf qshaix-picoctf   117 Sep 29 19:19 .
drwxr-xr-x 3 root           root              28 Sep 29 16:24 ..
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf  3771 Sep 29 16:24 .bashrc
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   807 Sep 29 16:24 .profile
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   167 Sep 29 16:25 .wget-hsts
-rw-r--r-- 1 root           root            4443 Sep 29 19:06 README.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf 10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$ chmod +x warm
qshaix-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
qshaix-picoctf@webshell:~$ ```
```


## Notas adicionales

## Referencias
