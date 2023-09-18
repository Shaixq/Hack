# Level 16

## Objetivo

The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso

bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1


## Solucion
``` bash
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 18:19 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00017s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.17 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: EF8E18828BCCF851651C9E8A9B5C245EE701E0CB484642A30D88B352A9FCF4CB
    Session-ID-ctx: 
    Resumption PSK: 683B2B012E6711FD8DD8329C1CE63A9081B21F79E6C68DD3F1C17441B82763EE1AE6A9518457C18004AC1D1DD2AC09AE
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 61 73 ea 5e 39 50 3f a5-29 13 e0 12 b7 a8 8e 80   as.^9P?.).......
    0020 - 1b b8 d5 3d ec d1 62 25-92 49 c0 25 7d c9 f7 4e   ...=..b%.I.%}..N
    0030 - 11 59 57 35 ed 89 b5 b4-64 b2 a5 cf f5 22 87 00   .YW5....d...."..
    0040 - 09 00 e2 81 64 f8 89 39-6a 33 08 76 d9 16 60 7d   ....d..9j3.v..`}
    0050 - e1 0e 80 ce a3 52 94 21-76 f4 f1 ad 8b 21 e2 07   .....R.!v....!..
    0060 - 3b 2a 36 8d fb 57 a2 bf-7d 39 ee 74 68 0c 38 6b   ;*6..W..}9.th.8k
    0070 - 47 3a d7 77 7d bb d1 59-94 d9 a6 65 41 62 a3 c5   G:.w}..Y...eAb..
    0080 - b3 6f 01 71 9b 5c 03 ce-84 08 0a 03 f7 7a 7d 7c   .o.q.\.......z}|
    0090 - 9a b2 78 98 5f 82 4e d4-59 de 79 42 be 34 ac bd   ..x._.N.Y.yB.4..
    00a0 - 3b 9a 78 37 ce 86 2c 61-d8 da e0 a4 7a 09 74 8d   ;.x7..,a....z.t.
    00b0 - 1d 87 7a 3e 39 08 74 4c-f3 11 73 8a 96 3c 82 74   ..z>9.tL..s..<.t
    00c0 - 94 e8 b0 1f b8 d7 47 6b-39 6a 5a 4b 32 af 44 aa   ......Gk9jZK2.D.

    Start Time: 1677176478
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 18CFB5C4D79B653E485630420D21B5C2B2B0BB37E2A0F00F9286A55DB37EC3AD
    Session-ID-ctx: 
    Resumption PSK: 0D29E51CD7A2D2A260FBC47FCE1B322DB78E8580BC66F6FF86471176BCC3647D5818CE89BDF3B2D23901B5B2EBADE343
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 79 ed 2b 98 64 8d 23 16-cb 67 23 88 a1 e5 90 7b   y.+.d.#..g#....{
    0020 - 23 33 c2 b2 4c 57 ae dd-64 e2 f9 6b e9 a9 11 b4   #3..LW..d..k....
    0030 - 65 0c 49 96 44 22 87 3a-01 97 21 4f 01 bd 84 57   e.I.D".:..!O...W
    0040 - e1 7b 8c d8 10 26 0f 67-6a 3a c2 37 4f 21 ac 21   .{...&.gj:.7O!.!
    0050 - 01 63 d1 4a 78 90 d3 cb-24 ff dd 1c f1 62 ef c3   .c.Jx...$....b..
    0060 - 93 0a fe 37 d0 f7 3d 9f-ac 85 ac b6 e4 93 6f 50   ...7..=.......oP
    0070 - e4 13 0b 89 35 45 f1 68-bc d7 49 9e 09 88 81 b5   ....5E.h..I.....
    0080 - 4e e8 cc f6 2b 74 71 81-fc 88 4b 92 aa 00 30 29   N...+tq...K...0)
    0090 - 85 74 4c c3 18 b1 a0 e3-e1 bf bb 43 60 ba 1f 95   .tL........C`...
    00a0 - b6 a6 df 93 59 e4 7d eb-1a 88 b0 a4 a6 1a 4e 56   ....Y.}.......NV
    00b0 - 66 fa 5e d1 79 6f 5f 79-c5 11 c4 45 7d 46 ff 9d   f.^.yo_y...E}F..
    00c0 - 25 ab 83 bb 41 87 de ca-db d2 93 e6 a1 53 45 e6   %...A........SE.

    Start Time: 1677176478
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed '

┌──(kali㉿kali)-[~/Documents]
└─$ ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p2220

bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ exit
```

## Notas adicionales

| comado | descripcion |
|----------|-------------|
| ---| ---
|

## Referencias