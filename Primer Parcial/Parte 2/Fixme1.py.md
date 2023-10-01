### Objetivos 
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)

### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2023-10-01 04:14:24--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.42, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py.2'

fixme1.py.2                                    100%[===================================================================================================>]     837  --.-KB/s    in 0s      

2023-10-01 04:14:24 (38.7 MB/s) - 'fixme1.py.2' saved [837/837]

qshaix-picoctf@webshell:~$ ls -la
total 164
drwxr-xr-x 5 qshaix-picoctf qshaix-picoctf  4096 Oct  1 04:14 .
drwxr-xr-x 3 root           root              28 Sep 29 16:24 ..
-rw------- 1 qshaix-picoctf qshaix-picoctf   631 Sep 29 20:29 .bash_history
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf  3771 Sep 29 16:24 .bashrc
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1024 Oct  1 04:13 .fixme1.py.swp
drwxrwxr-x 3 qshaix-picoctf qshaix-picoctf    19 Oct  1 04:08 .local
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   807 Sep 29 16:24 .profile
drwx------ 2 qshaix-picoctf qshaix-picoctf    48 Sep 29 20:06 .ssh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   215 Oct  1 04:05 .wget-hsts
drwxr-xr-x 3 qshaix-picoctf qshaix-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root            4443 Oct  1 04:14 README.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf 14551 Oct 26  2020 file
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   837 Mar 16  2023 fixme1.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   837 Mar 16  2023 fixme1.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   837 Mar 16  2023 fixme1.py.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    34 Mar 16  2021 flag
-rwxrwxrwx 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1668 Sep 29 19:43 static.ltdis.strings.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  6497 Sep 29 19:43 static.ltdis.x86_64.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf 10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$ python3 fixme1.py
  File "/home/qshaix-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
qshaix-picoctf@webshell:~$ nano fixme1.py
qshaix-picoctf@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
	picoCTF{1nd3nt1ty_cr1515_6a476c8f} 
### Notas adicionales:



### Referencias:
