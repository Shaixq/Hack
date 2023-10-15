### Objetivos 
There is some interesting information hidden around this site [http://mercury.picoctf.net:5080/](http://mercury.picoctf.net:5080/). Can you find it?

### Solución 

``` bash
entramos a view source y entre el código buscamos las pistas 
1: <!-- Here's the first part of the flag: picoCTF{t -->

en el css encontramos otra parte
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */

cambiamo el final del link por /robots.txt 
# Part 3: t_0f_pl4c

cambiamo el final del link por /.htaccess
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.

cambiamo el final del link por .DS_Store
Part 5: _35844447}


```

### Notas adicionales:

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_35844447}