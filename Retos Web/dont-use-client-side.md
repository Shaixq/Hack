### Objetivos 

Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/37821/` ([link](https://jupiter.challenges.picoctf.org/problem/37821/)) or http://jupiter.challenges.picoctf.org:37821
### Solución 

``` bash
Entrar al link proporcionado y ver el código fuente y ver que me da la bandera en partes
|---|
|if (checkpass.substring(0, split) == 'pico') {|
||if (checkpass.substring(split*6, split*7) == 'a3c8') {|
||if (checkpass.substring(split, split*2) == 'CTF{') {|
||if (checkpass.substring(split*4, split*5) == 'ts_p') {|
||if (checkpass.substring(split*3, split*4) == 'lien') {|
||if (checkpass.substring(split*5, split*6) == 'lz_1') {|
||if (checkpass.substring(split*2, split*3) == 'no_c') {|
||if (checkpass.substring(split*7, split*8) == '9}') {|

```

### Notas adicionales:

picoCTF{no_clients_plz_1a3c89}

### Referencias: