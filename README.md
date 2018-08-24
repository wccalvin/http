# HTTP: **H**yper**T**ext **T**ransfer **P**rotocol
> Rules that govern how two devices should communicate with each other over the
internet

## Using telnet to demonstrate Request <-> Response cycle

### Request Samples
```console
http 🔥 telnet httpbin.org 80
Trying 34.239.63.98...
Connected to httpbin.org.
Escape character is '^]'.
GET / HTTP/1.1
Host: httpbin.org
```


```console
http 🔥 telnet httpbin.org 80
Trying 52.204.188.97...
Connected to httpbin.org.
Escape character is '^]'.
GET /xml HTTP/1.1
Host: httpbin.org
```

### Response Samples
```console
HTTP/1.1 200 OK
Connection: keep-alive
Server: gunicorn/19.9.0
Date: Fri, 24 Aug 2018 02:23:01 GMT
Content-Type: application/xml
Content-Length: 522
Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true
Via: 1.1 vegur
```

* Note:
    * HTTP is stateless - it does not remember the previous request