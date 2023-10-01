### Objetivos 

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)
### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2023-10-01 04:01:32--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                   100%[===================================================================================================>]   1.16K  --.-KB/s    in 0s      

2023-10-01 04:01:32 (47.9 MB/s) - 'convertme.py' saved [1189/1189]

qshaix-picoctf@webshell:~$ ls -la
total 132
drwxr-xr-x 4 qshaix-picoctf qshaix-picoctf  4096 Oct  1 04:01 .
drwxr-xr-x 3 root           root              28 Sep 29 16:24 ..
-rw------- 1 qshaix-picoctf qshaix-picoctf   631 Sep 29 20:29 .bash_history
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf  3771 Sep 29 16:24 .bashrc
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   807 Sep 29 16:24 .profile
drwx------ 2 qshaix-picoctf qshaix-picoctf    48 Sep 29 20:06 .ssh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   167 Sep 29 16:25 .wget-hsts
drwxr-xr-x 3 qshaix-picoctf qshaix-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root            4443 Oct  1 04:01 README.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    34 Mar 16  2021 flag
-rwxrwxrwx 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1668 Sep 29 19:43 static.ltdis.strings.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  6497 Sep 29 19:43 static.ltdis.x86_64.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf 10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$  python3 convertme.py 
If 64 is in decimal base, what is it in binary base?
Answer: 1000000
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
```

### Notas adicionales:



### Referencias:
