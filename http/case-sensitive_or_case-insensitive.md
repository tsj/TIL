# case-sensitive

HTTP-version is case-sensitive. [[RFC7230]](https://tools.ietf.org/html/rfc7230#page-14)
```
HTTP/1.1
```

The request method is case-sensitive. [[RFC7230]](https://tools.ietf.org/html/rfc7230#page-21) [[RFC 7231]](https://tools.ietf.org/html/rfc7231#section-4)
```
GET
HEAD
POST
PUT
DELETE
CONNECT
OPTIONS
TRACE
```

Test
```
❯ curl -v -X get http://www.google.com
* Rebuilt URL to: http://www.google.com/
*   Trying 216.58.192.4...
* Connected to www.google.com (216.58.192.4) port 80 (#0)
> get / HTTP/1.1
> Host: www.google.com
> User-Agent: curl/7.43.0
> Accept: */*
>
< HTTP/1.1 405 Method Not Allowed
< Content-Type: text/html; charset=UTF-8
< Content-Length: 1588
< Date: Tue, 12 Jul 2016 05:54:58 GMT
<

...

* Connection #0 to host www.google.com left intact
```

# case-insensitive

Each header field consists of a case-insensitive field name followed by a colon (":"), optional leading whitespace, the field value, and optional trailing whitespace.
[[RFC7230]](https://tools.ietf.org/html/rfc7230#section-3.2)

