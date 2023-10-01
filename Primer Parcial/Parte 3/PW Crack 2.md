### Objetivos 

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.py
--2023-10-01 04:46:58--  https://artifacts.picoctf.net/c/14/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.93, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                      100%[===================================================================================================>]     914  --.-KB/s    in 0s      

2023-10-01 04:46:58 (250 MB/s) - 'level2.py' saved [914/914]

qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
--2023-10-01 04:47:08--  https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.18, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                            100%[===================================================================================================>]      31  --.-KB/s    in 0s      

2023-10-01 04:47:08 (15.1 MB/s) - 'level2.flag.txt.enc' saved [31/31]

qshaix-picoctf@webshell:~$ nano level2.py
qshaix-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```

### Notas adicionales:
 user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) 
							4					e				c					9
4ec9

picoCTF{tr45h_51ng1ng_9701e681}
### Referencias: