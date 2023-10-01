### Objetivos 
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
--2023-10-01 03:54:35--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.42, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py.1'

code.py.1                                      100%[===================================================================================================>]   1.25K  --.-KB/s    in 0s      

2023-10-01 03:54:35 (56.5 MB/s) - 'code.py.1' saved [1278/1278]

qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2023-10-01 03:54:50--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.93, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt.1'

codebook.txt.1                                 100%[===================================================================================================>]      27  --.-KB/s    in 0s      

2023-10-01 03:54:50 (655 KB/s) - 'codebook.txt.1' saved [27/27]

qshaix-picoctf@webshell:~$ ls -la
total 128
drwxr-xr-x 4 qshaix-picoctf qshaix-picoctf  4096 Oct  1 03:54 .
drwxr-xr-x 3 root           root              28 Sep 29 16:24 ..
-rw------- 1 qshaix-picoctf qshaix-picoctf   631 Sep 29 20:29 .bash_history
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   220 Sep 29 16:24 .bash_logout
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf  3771 Sep 29 16:24 .bashrc
-rw-r--r-- 1 qshaix-picoctf qshaix-picoctf   807 Sep 29 16:24 .profile
drwx------ 2 qshaix-picoctf qshaix-picoctf    48 Sep 29 20:06 .ssh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   167 Sep 29 16:25 .wget-hsts
drwxr-xr-x 3 qshaix-picoctf qshaix-picoctf    28 Mar 16  2021 Addadshashanammu
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root           root            4443 Oct  1 03:54 README.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1278 Mar 16  2023 code.py.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    27 Mar 16  2023 codebook.txt.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf    34 Mar 16  2021 flag
-rwxrwxrwx 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1668 Sep 29 19:43 static.ltdis.strings.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  6497 Sep 29 19:43 static.ltdis.x86_64.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf 10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$  chmod +x code.py
qshaix-picoctf@webshell:~$  ./code.py
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
./code.py: line 7: syntax error near unexpected token `('
./code.py: line 7: `def str_xor(secret, key):'
qshaix-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_7d102d7a}
```
picoCTF{c0d3b00k_455157_7d102d7a}
### Notas adicionales:



### Referencias:
