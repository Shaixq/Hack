# Level 11

## Objetivo

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso

bandit11
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Solucion
Forma 1
``` bash

bandit11@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit12 bandit11   49 Jan 11 19:18 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit11@bandit:~$ cat data.txt 
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
Forma 2
``` python
bandit11@bandit:~$ python3
Python 3.10.6 (main, Nov 14 2022, 16:10:14) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import codecs
>>> cadena=open('data.txt').read()
>>> codecs.decode(cadena,'rot13')
'The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv\n'

```
## Notas adicionales

| comado | descripcion |
|----------|-------------|
| ---| ---
|

