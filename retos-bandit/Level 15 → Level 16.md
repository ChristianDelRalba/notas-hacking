

## Objetivo

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos de acceso al nivel
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solución
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEIivS1jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC4
XC9dgne8ha9I/vXn4uTtObLhI/PPyLyl4jyDQPp61VtsEMcOb95KhXxdtQiDtzSD
3KXQVFLaPlVGKDWSR9nV+GoazSNPmNLH/IMVrUYxXjYikPxo1jjYKyuqfjV5bNm3
Hz6z4eDl7wNbPRaPAMPo0WU23m9M04bKQHLINfN7Abz3a+7ChLeICrWXiXp9mWfj
PY8cK7Vayz0eHU4Lg64q4jUaXQqZ/ta1RqZEwv7ZuTKctcazpK/u2+h4zvQCPyLh
uDjUXZTLlIuhfjyKUJLQsmYHAQprV6sY3ybFN32dW6MSE0/ApT6Th0LzKeaYxk5b
3NIeaYyPeKsjqFSwy+2zAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBQ
RXG1k+cB357X43fsiyaCQQh4RbWHOcg1jBes5eiC/H8MyC3ec1znXvOUfqJcWNQJ
9UJDMwbkpo+IcwJiOe9n/D3Zeypv1g+ta8KKLsQ+zcbp5RdltKy7GuO/s5WjVofE
/IHz/5g+IMoqqYLlquQ539CZykPMC9TB9uWfJj/i8faCox4gjtkSCri+27tUZuHi
eYR3zxY1ptsJti/pMaItC6Oc2/pSlotQ4fXdciLZYGXqlmSFBt8Y8/v1YkhME5gN
3HmBV/Zg1SghA57zYsbf3npvQwudr04f2iF493pe0VRN6DfiXTxWkJe1VKuyGHEr
Q4L4OdVlgMSeyYyKgFc7
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
    Session-ID: 2868798C3DE846676B32C78EBA9546A0E424E8950DF7805B4AD8463902161179
    Session-ID-ctx:
    Resumption PSK: 9A434DC44B4444B352668787AEBDDA7F4FD0C1C2C0CEC54FBC393B428EC0D9B543D6544C7499180A2AC36507402B22EE
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - b5 ab 10 f3 f4 14 6f 49-44 e1 06 b1 1e 08 ed d3   ......oID.......
    0020 - eb af da 03 89 61 3a c5-46 b4 ea 6e 53 d2 ee 05   .....a:.F..nS...
    0030 - 3e e9 ff 61 d0 a6 d6 18-36 e5 d2 23 60 6d 39 00   >..a....6..#`m9.
    0040 - 4e 9e 4c 3f 60 e9 c5 3c-ef fa 52 91 25 eb 45 71   N.L?`..<..R.%.Eq
    0050 - 23 68 af 63 a7 a8 d9 40-1c 0d f4 b6 4b bf 1c 84   #h.c...@....K...
    0060 - d7 3f 7f 81 1e d8 e3 aa-a0 ca 50 7f ac 9f 7b e3   .?........P...{.
    0070 - 66 5b 84 e4 39 92 13 df-73 eb 9e 64 43 19 f4 58   f[..9...s..dC..X
    0080 - 0b ad da 6a 67 66 b7 f7-51 4f fb 80 ae a0 29 77   ...jgf..QO....)w
    0090 - c2 76 ce 70 d4 46 19 a4-6a cb 6e de 40 4c 2d bb   .v.p.F..j.n.@L-.
    00a0 - 52 db 4c d9 c4 08 54 f2-ec c5 2d 80 ee 9e 1f 62   R.L...T...-....b
    00b0 - 60 c1 80 3f f3 23 c8 75-51 ff 5a 56 c6 ea ed 8d   `..?.#.uQ.ZV....
    00c0 - 74 c3 47 5e 0f 8b 05 ee-0e a1 c0 9e 96 47 3e a5   t.G^.........G>.

    Start Time: 1708455165
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
    Session-ID: 79146F437DDED06D5A841B1FC40E134AF5EE85A11C65D6101C6983BBB2A4627A
    Session-ID-ctx:
    Resumption PSK: 6AC650112BAF74FE3458C7F46F759FE5B10918291CF132541802C7F8AC37BA5E550EACCCF949EABDEE98C5F8C02B80E6
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 81 c9 7a 81 90 61 a2 44-6e 83 ab 39 4b a2 9f d6   ..z..a.Dn..9K...
    0010 - a1 4f ef 1d 37 c2 59 e4-a8 cb 04 67 97 c4 ef 9f   .O..7.Y....g....
    0020 - e0 14 76 55 2f 8a 43 36-c0 67 01 c4 6b 41 7a cc   ..vU/.C6.g..kAz.
    0030 - 30 50 04 64 2d f8 ee ea-85 db dd 17 74 e1 46 4e   0P.d-.......t.FN
    0040 - 36 98 94 d2 c3 cd 78 d0-b8 01 ed 89 1e d1 70 f9   6.....x.......p.
    0050 - 2f 82 c6 c8 e8 85 0c f3-e9 69 f3 b3 96 ac ab be   /........i......
    0060 - af 8f 6c 75 3a 1d 15 71-62 03 1d 7a 4d 3d 22 42   ..lu:..qb..zM="B
    0070 - 31 fa 9a 87 eb 3c ad 5c-cb 3c 58 36 f8 8e 79 13   1....<.\.<X6..y.
    0080 - 7a 18 6d be 91 6f 48 91-15 90 f6 d0 9a 14 e4 e6   z.m..oH.........
    0090 - ba a2 e3 85 7c e7 7c 21-88 18 46 77 a2 cd e8 8f   ....|.|!..Fw....
    00a0 - ad c6 3e f9 63 5c e0 ae-30 a9 83 a3 14 7e 1a d2   ..>.c\..0....~..
    00b0 - a7 39 98 03 55 a5 0e ee-e8 c8 ba ec ba 08 ba 4f   .9..U..........O
    00c0 - 55 7f 98 c7 e0 40 2a c5-ca ea 67 0f cb 4d 74 19   U....@*...g..Mt.

    Start Time: 1708455165
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
bandit15@bandit:~$

## Notas adicionales

## Referencias
