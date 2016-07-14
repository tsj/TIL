# Test TLS connection

```
$ openssl s_client -connect <HOST_NAME>:<PORT>
```

Test
```
$ openssl s_client -connect www.google.com:443
CONNECTED(00000003)
depth=2 /C=US/O=GeoTrust Inc./CN=GeoTrust Global CA
verify error:num=20:unable to get local issuer certificate
verify return:0
---
Certificate chain
 0 s:/C=US/ST=California/L=Mountain View/O=Google Inc/CN=www.google.com
   i:/C=US/O=Google Inc/CN=Google Internet Authority G2
 1 s:/C=US/O=Google Inc/CN=Google Internet Authority G2
   i:/C=US/O=GeoTrust Inc./CN=GeoTrust Global CA
 2 s:/C=US/O=GeoTrust Inc./CN=GeoTrust Global CA
   i:/C=US/O=Equifax/OU=Equifax Secure Certificate Authority
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIEgDCCA2igAwIBAgIIf5aDi9aJCnMwDQYJKoZIhvcNAQELBQAwSTELMAkGA1UE
BhMCVVMxEzARBgNVBAoTCkdvb2dsZSBJbmMxJTAjBgNVBAMTHEdvb2dsZSBJbnRl
cm5ldCBBdXRob3JpdHkgRzIwHhcNMTYwNzA2MDgxODEwWhcNMTYwOTI4MDgwMzAw
WjBoMQswCQYDVQQGEwJVUzETMBEGA1UECAwKQ2FsaWZvcm5pYTEWMBQGA1UEBwwN
TW91bnRhaW4gVmlldzETMBEGA1UECgwKR29vZ2xlIEluYzEXMBUGA1UEAwwOd3d3
Lmdvb2dsZS5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCugUi6
O/18iE3fI8JOGd7wSJQx7yUc5kx1TD3YlLr5nNWH521cd+3gInCL+u1mL5/V7YuH
AmDOzGP7sVBTDWw5F41CpuOdvgWDd3ADsbQZuycQR9ma44Wh6fn7cbdAldUm2fIO
JI7TpG0M/DsZRfAy7S3tvJydw69Ftxx1cWVB2LDGNySlJKbrUsbj8lZVGAlMt8pC
zRM74arc2ye7VxhYGGA7nHY8daZZlSNJwj0rUSzXcI6R8d9Np84XT3EgBx7IcFZi
pCJUMaVNnK6Tge7rGApEsZ9tZJ7JuI9ip2Y6PAA9owMEbksLmxRZL6nBAKvnJnbE
Jn26b5W7tSDA6bcfAgMBAAGjggFLMIIBRzAdBgNVHSUEFjAUBggrBgEFBQcDAQYI
KwYBBQUHAwIwGQYDVR0RBBIwEIIOd3d3Lmdvb2dsZS5jb20waAYIKwYBBQUHAQEE
XDBaMCsGCCsGAQUFBzAChh9odHRwOi8vcGtpLmdvb2dsZS5jb20vR0lBRzIuY3J0
MCsGCCsGAQUFBzABhh9odHRwOi8vY2xpZW50czEuZ29vZ2xlLmNvbS9vY3NwMB0G
A1UdDgQWBBS1TkLw9DZULCRuBAs7CMFcqGYwhDAMBgNVHRMBAf8EAjAAMB8GA1Ud
IwQYMBaAFErdBhYbvPZotXb1gba7Yhq6WoEvMCEGA1UdIAQaMBgwDAYKKwYBBAHW
eQIFATAIBgZngQwBAgIwMAYDVR0fBCkwJzAloCOgIYYfaHR0cDovL3BraS5nb29n
bGUuY29tL0dJQUcyLmNybDANBgkqhkiG9w0BAQsFAAOCAQEABaAbGotP8/tKWkHU
6+Wv657N4QZfDgjmVAJpNXUsAmH8TxpPlSQR0d+Fa9TJtaTSOd+CWOirjwWo9eXu
JAvjT+nw3Y2o+TxJWc1lY+C0C2aKtVh88vn5fCzWr1+xn+fN1AhBytTjuy1D3COY
/KzJHNYXrTYqVn8+VcXiVat9TYLJ5uYF88Nhww3oJIk9KnSeA4RO6yZojkBug0S/
3kK8MkCMqCklU+8e11XdIvRg9T/wfz5IMNFDFWHzCDpprDX6MUJT/II8cfHhRhtp
1oVDwI7xy6Lgh5Kemse17Ff7w1j5jmN+/0M4PDaU9e8U+/7lFanoQ+s3L8eMMZ24
HqW9MQ==
-----END CERTIFICATE-----
subject=/C=US/ST=California/L=Mountain View/O=Google Inc/CN=www.google.com
issuer=/C=US/O=Google Inc/CN=Google Internet Authority G2
---
No client certificate CA names sent
---
SSL handshake has read 3240 bytes and written 456 bytes
---
New, TLSv1/SSLv3, Cipher is AES128-SHA
Server public key is 2048 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
SSL-Session:
    Protocol  : TLSv1
    Cipher    : AES128-SHA
    Session-ID: 998EE793E76A87479E082A8C40AB83544D0B1CDAE16967E8B8A76E193253165A
    Session-ID-ctx:
    Master-Key: 8F87955FD44A41CE1D7D9D42962DC61FE7CA35385D338BCE421635AA566CA9367EACDC7FB5A9C45D38384D2FF79141AC
    Key-Arg   : None
    Start Time: 1468479335
    Timeout   : 300 (sec)
    Verify return code: 0 (ok)
---

waiting input...
```

If you type a HTTP request message, the server responds your request message.
(For sending you should type enter twice.)

```
GET / HTTP/1.1
Host: www.google.com
Connection: keep-alive

HTTP/1.1 200 OK
Date: Thu, 14 Jul 2016 06:58:38 GMT
Expires: -1
Cache-Control: private, max-age=0
Content-Type: text/html; charset=ISO-8859-1
P3P: CP="This is not a P3P policy! See https://www.google.com/support/accounts/answer/151657?hl=en for more info."
Server: gws
X-XSS-Protection: 1; mode=block
X-Frame-Options: SAMEORIGIN
Set-Cookie: NID=82=n9xb9nUgdO-TAYkdg08gzzy-H7Y8L2dJc4jL3soLzZYhPHLyEl92VxTZDSwRjNU1mzU-Clth-OW4d5gHQaAiXCrQP4ra9X7-T-Cr2JkN-weRSxo3Vl-FLO68QocXNDt4mWXGRi4wC07s5W8; expires=Fri, 13-Jan-2017 06:58:38 GMT; path=/; domain=.google.com; HttpOnly
Alternate-Protocol: 443:quic
Alt-Svc: quic=":443"; ma=2592000; v="36,35,34,33,32,31,30,29,28,27,26,25"
Accept-Ranges: none
Vary: Accept-Encoding
Transfer-Encoding: chunked

8000
<!doctype h ...

Connection was still connected
```

```
GET / HTTP/1.0
Host: www.google.com

HTTP/1.0 200 OK
Date: Thu, 14 Jul 2016 06:59:56 GMT
Expires: -1
Cache-Control: private, max-age=0
Content-Type: text/html; charset=ISO-8859-1
P3P: CP="This is not a P3P policy! See https://www.google.com/support/accounts/answer/151657?hl=en for more info."
Server: gws
X-XSS-Protection: 1; mode=block
X-Frame-Options: SAMEORIGIN
Set-Cookie: NID=82=fYOJEJ30sWrOwXtdYPqqNA43-0PvEf6Y2wPAEwIoYqpUHudOFf2DVco27ZjS5LYrYybSMNlXBI8fvN3Iqr1NJnVTN0UyoEd-05-HEX8g8S1LI8X9ucdp21A_IZWK6wKboftiWnkLcU5Ah3A; expires=Fri, 13-Jan-2017 06:59:56 GMT; path=/; domain=.google.com; HttpOnly
Alternate-Protocol: 443:quic
Alt-Svc: quic=":443"; ma=2592000; v="36,35,34,33,32,31,30,29,28,27,26,25"
Accept-Ranges: none
Vary: Accept-Encoding

<!doctype html><html ...

Connection was closed
```

reference: https://liquidat.wordpress.com/2013/03/15/short-tip-test-tls-connections-on-command-line/
