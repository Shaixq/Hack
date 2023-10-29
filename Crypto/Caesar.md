### Objetivos 

#### Description

Decrypt this [message](https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext).

### Solución 

```
┌──(kali㉿kali)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
--2023-10-29 16:03:42--      

2023-10-29 16:03:43 (16.7 MB/s) - ‘ciphertext’ saved [35/35]

                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ cat ciphertext 
picoCTF{dspttjohuifsvcjdpoabrkttds}           
Pero esta bandera no es aceptada, intentamos rotandola con rot13 hasta que sea algo leíble y sale hasta rotarla 25 veces 

crossingtherubiconzaqjsscr


```

### Notas adicionales:

picoCTF{crossingtherubiconzaqjsscr}

### Referencias: