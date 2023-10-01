### Objetivos 

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.
### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2023-10-01 04:55:49--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.18, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                       100%[===================================================================================================>]     270  --.-KB/s    in 0s      

2023-10-01 04:55:49 (14.2 MB/s) - 'runme.py' saved [270/270]

qshaix-picoctf@webshell:~$ python3 runme.py
picoCTF{run_s4n1ty_run}
```

### Notas adicionales:
picoCTF{run_s4n1ty_run}


### Referencias:
	