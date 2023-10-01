### Objetivos 

Our flag printing service has started glitching!`$ nc saturn.picoctf.net 49700`
### Solución 

``` bash
qshaix-picoctf@webshell:~$ nc saturn.picoctf.net 49700
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

```

### Notas adicionales:

chr(0x61) = a
chr(0x34) = 4
chr(0x33) = 3
chr(0x39) = 9
chr(0x32) = 2
chr(0x64) = d
chr(0x32) = 2
chr(0x65) = e

picoCTF{gl17ch_m3_n07_a4392d2e}
### Referencias:
