### Objetivos 

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
--2023-10-01 04:05:23--  https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                                           100%[===================================================================================================>]  14.21K  --.-KB/s    in 0s      

2023-10-01 04:05:23 (438 MB/s) - 'file' saved [14551/14551]

qshaix-picoctf@webshell:~$ ls -la
total 148
drwxr-xr-x 4 qshaix-picoctf qshaix-picoctf  4096 Oct  1 04:05 .
drwxr-xr-x 3 root           root              28 Sep 29 16:24 ..
-rw------- 1 qshaix-picoctf qshaix-picoctf   631 Sep 29 20:29 .bash_history
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf  3771 Sep 29 16:24 .bashrc
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   807 Sep 29 16:24 .profile
drwx------ 2 qshaix-picoctf qshaix-picoctf    48 Sep 29 20:06 .ssh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   215 Oct  1 04:05 .wget-hsts
drwxr-xr-x 3 qshaix-picoctf qshaix-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root            4443 Oct  1 04:05 README.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf 14551 Oct 26  2020 file
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    34 Mar 16  2021 flag
-rwxrwxrwx 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1668 Sep 29 19:43 static.ltdis.strings.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  6497 Sep 29 19:43 static.ltdis.x86_64.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf 10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$ cat file | grep pico
picoCTF{grep_is_good_to_find_things_dba08a45}
```
picoCTF{grep_is_good_to_find_things_dba08a45}
### Notas adicionales:



### Referencias:
