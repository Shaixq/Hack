### Objetivos 
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

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
qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
--2023-10-01 04:18:24--  https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                        100%[===================================================================================================>] 757.84K  1.85MB/s    in 0.4s    

2023-10-01 04:18:24 (1.85 MB/s) - 'strings' saved [776032/776032]

qshaix-picoctf@webshell:~$ ls -la
total 920
drwxr-xr-x 5 qshaix-picoctf qshaix-picoctf   4096 Oct  1 04:18 .
drwxr-xr-x 3 root           root               28 Sep 29 16:24 ..
-rw------- 1 qshaix-picoctf qshaix-picoctf    631 Sep 29 20:29 .bash_history
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf    220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   3771 Sep 29 16:24 .bashrc
drwxrwxr-x 3 qshaix-picoctf qshaix-picoctf     19 Oct  1 04:08 .local
qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
--2023-10-01 04:27:54--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                      100%[===================================================================================================>]   1.00K  --.-KB/s    in 0s      

2023-10-01 04:27:54 (309 MB/s) - 'fixme2.py' saved [1029/1029]

qshaix-picoctf@webshell:~$ ls -la 
total 924
drwxr-xr-x 5 qshaix-picoctf qshaix-picoctf   4096 Oct  1 04:27 .
drwxr-xr-x 3 root           root               28 Sep 29 16:24 ..
-rw------- 1 qshaix-picoctf qshaix-picoctf    631 Sep 29 20:29 .bash_history
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf    220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   3771 Sep 29 16:24 .bashrc
drwxrwxr-x 3 qshaix-picoctf qshaix-picoctf     19 Oct  1 04:08 .local
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf    807 Sep 29 16:24 .profile
drwx------ 2 qshaix-picoctf qshaix-picoctf     48 Sep 29 20:06 .ssh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    167 Oct  1 04:18 .wget-hsts
drwxr-xr-x 3 qshaix-picoctf qshaix-picoctf     28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root             4443 Oct  1 04:14 README.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf   1278 Mar 16  2023 code.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   1278 Mar 16  2023 code.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf     27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf     27 Mar 16  2023 codebook.txt.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    835 Oct  1 04:15 fixme1.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    837 Mar 16  2023 fixme1.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    837 Mar 16  2023 fixme1.py.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   1029 Mar 16  2023 fixme2.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf     34 Mar 16  2021 flag
-rwxrwxrwx 1 qshaix-picoctf qshaix-picoctf    785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf   8376 Mar 16  2021 static
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   8376 Mar 16  2021 static.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   8376 Mar 16  2021 static.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   1668 Sep 29 19:43 static.ltdis.strings.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   6497 Sep 29 19:43 static.ltdis.x86_64.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf 776032 Oct 26  2020 strings
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$ nano fixme2.py
qshaix-picoctf@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
### Notas adicionales:



### Referencias:
