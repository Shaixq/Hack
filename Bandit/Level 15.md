# Level 15

## Objetivo

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos de acceso

bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## Solucion
``` bash

bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:56 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:56 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:56 2023 GMT; NotAfter: Feb 21 22:03:56 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEF3vcjDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU2WhcNMjMwMjIxMjIwMzU2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCg
1elREdWTbtCZNl7KNMjleNrcG71f9lZhjAfM4x+TDwlPpT+Q9O3V6J687fJdMH85
xfUwcZG0XFCeN1nxnmQadGF/ZHEt0laWmCQfo5LogzgGFcaZWC1a6XZ5ZKv7SRDt
tvPK/CTKwOJD5ZJVEXEk9R8YQ/VbKwZMDc43WD/HKypvBv7fZVbJkKYY75LOby86
7gux29Emhntj5pZyYagYbmonnAiw6447bGTC1d6jilGPhXMzckTI57WGeNdp4ppL
3pXSVDLOU2XJ8Um/L2VIgGTsUk5CwrtzVxyt6I5sKavUhsNGlzqvHI/McgbsnHi8
3LDg9k/Co8F21eZFooVlAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBz
lgp6XhMshglRxhxHRg1xHkVYSFSBaS5Adq5OIoE/oetyedTiO2B9MLmNZ9Juu/WK
/+WZFmNdzQ6Iw5ueBz/rmY+DvzTjjd4CPPqeilG5mngceR5nliM9mXkpQlmm3T1a
8JuBrDugrN9BP4IeBTER0pgQcQvsRATrv/SAVFVBhTSvOKFhoYNEdBzaqxclEjD6
bl3UkzNag/S3iLuv24xoQkMmlFC2afaswkG/cQ4p3BuapuZORjbohUOXS24QDl0z
A2RDFNizi42ZVJ8ZW1qbURZ4n/VbIAi7vRHldPKjC8hYAcdvUekB0schBlc1J06Z
phGCgzTVUzJu9yz8uKzO
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
    Session-ID: C325BABB568B219843897BA095E6221A576AF73CD52151653F5B8080F9B46A96
    Session-ID-ctx: 
    Resumption PSK: 002780CEFC0962A4998EEE38AE92B416162F3547204E79AE06AF401F13CD06327484722CDD4F221F673944982F2A76CD
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - a5 3d 92 1f d1 78 36 48-bb a6 da 4d 19 13 ee a7   .=...x6H...M....
    0010 - 8d d3 64 03 42 63 03 d1-6f 49 52 22 54 86 57 bd   ..d.Bc..oIR"T.W.
    0020 - c6 5e 2b 81 ad bc e7 75-a7 96 3a db 46 a7 91 06   .^+....u..:.F...
    0030 - 4a 09 bc ee f5 77 9a ee-df 96 51 4e 93 42 50 69   J....w....QN.BPi
    0040 - d7 8c 30 57 ca 98 1b b1-6a a9 41 35 b2 87 d3 2a   ..0W....j.A5...*
    0050 - 2e 7b 1d a8 e4 a5 5c 9a-bf d2 88 82 45 eb f4 af   .{....\.....E...
    0060 - 34 6c 8c 64 f2 0e 07 f9-ca ac e4 31 4f 91 a8 f6   4l.d.......1O...
    0070 - 4d 53 3c f9 1e 4d e1 f8-d5 ce 96 3f 6f 8a 30 24   MS<..M.....?o.0$
    0080 - e0 de 8c 23 c5 f7 82 45-57 24 06 df bc 20 59 71   ...#...EW$... Yq
    0090 - 4c 8b 55 df 19 42 5b 7f-92 43 89 c8 23 f0 98 13   L.U..B[..C..#...
    00a0 - 71 09 b9 74 7d 50 e1 44-0f 3d da 1e a0 55 ac c8   q..t}P.D.=...U..
    00b0 - 6b d3 67 48 33 84 a7 10-3c 66 f9 53 91 e1 84 9b   k.gH3...<f.S....
    00c0 - 20 82 68 ed 1b d5 67 53-34 69 0b 20 d0 40 fb 7a    .h...gS4i. .@.z

    Start Time: 1677123617
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
    Session-ID: 656ADE03B39AAEDF0A4EA256BFF4D6E406121E59550422E8C9DA3C1D8CBBFA2F
    Session-ID-ctx: 
    Resumption PSK: EE0D8C4B9DDAFA486E986A72553C4E36AB909F9450B115A96D1BD6E3333D70C57D39B8B909BB429E1046446DFFFD7E89
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - a5 3d 92 1f d1 78 36 48-bb a6 da 4d 19 13 ee a7   .=...x6H...M....
    0010 - 46 74 36 2f c9 b9 88 36-a4 fb 7b e8 ec 78 f3 5a   Ft6/...6..{..x.Z
    0020 - 62 61 6c b1 8e e0 69 e8-ee 29 bb ff 7c e7 85 2d   bal...i..)..|..-
    0030 - 8f f2 10 32 5c 22 82 8e-f8 28 55 26 ba 6a 51 61   ...2\"...(U&.jQa
    0040 - 11 ef 5d a7 e2 36 79 59-64 3b dd d9 9d 74 e7 9e   ..]..6yYd;...t..
    0050 - 51 7f cf 24 75 bc 1b 15-24 fb 4b f5 1b d7 c4 b2   Q..$u...$.K.....
    0060 - dd 3b d2 07 84 9b 2c 57-d2 4b 3c bd 42 b3 20 e0   .;....,W.K<.B. .
    0070 - b8 84 df 28 bd 60 09 ad-7e 28 73 32 55 00 b3 1e   ...(.`..~(s2U...
    0080 - 59 ee 10 91 c2 c6 2a b1-b5 d3 88 a6 fa 3f ca 46   Y.....*......?.F
    0090 - e6 8e 8c 53 da 71 17 35-09 0e 2d d5 f2 da 5f f8   ...S.q.5..-..._.
    00a0 - 9f 6f 93 ef 90 62 e5 8e-2b f3 1d 27 bf e5 35 c4   .o...b..+..'..5.
    00b0 - 92 cd 30 e0 a4 09 9c 75-fb b9 b0 0c b2 7e 6a cd   ..0....u.....~j.
    00c0 - 47 bb 0f bb 5f 12 fa ff-d6 c1 b4 82 1f e2 b7 c2   G..._...........

    Start Time: 1677123617
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed

```

## Notas adicionales

| comado | descripcion |
|----------|-------------|
| ---| ---
|

## Referencias