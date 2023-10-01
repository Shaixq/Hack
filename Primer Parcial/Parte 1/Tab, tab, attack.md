### Objetivos 
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames:
### Solución 
wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
--2023-09-29 19:40:41--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static.2'

static.2                                       100%[===================================================================================================>]   8.18K  --.-KB/s    in 0s      

2023-09-29 19:40:41 (251 MB/s) - 'static.2' saved [8376/8376]

qshaix-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
--2023-09-29 19:41:44--  https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh.1'

qshaix-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
--2023-09-29 19:49:03--  https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                           100%[===================================================================================================>]   4.41K  --.-KB/s    in 0s      

2023-09-29 19:49:03 (1.73 GB/s) - 'Addadshashanammu.zip' saved [4520/4520]

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
-rwxrwxrwx 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf   785 Mar 16  2021 ltdis.sh.1
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.1
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  8376 Mar 16  2021 static.2
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  1668 Sep 29 19:43 static.ltdis.strings.txt
-rw-rw-r-- 1 qshaix-picoctf qshaix-picoctf  6497 Sep 29 19:43 static.ltdis.x86_64.txt
-rwxrwxr-x 1 qshaix-picoctf qshaix-picoctf 10936 Mar 16  2021 warm
qshaix-picoctf@webshell:~$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
qshaix-picoctf@webshell:~$ ./fang-of-haynekhtnamet
-bash: ./fang-of-haynekhtnamet: No such file or directory
qshaix-picoctf@webshell:~$  cd Addadshashanammu/Almurbalarammi/AshalmimilkaAssurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
-bash: cd: Addadshashanammu/Almurbalarammi/AshalmimilkaAssurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/: No such file or directory
qshaix-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
qshaix-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
qshaix-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala
qshaix-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
qshaix-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
qshaix-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}



### Notas adicionales:



### Referencias:
