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

### Example of sending data with the GET request and the response recieved
```console
http 🔥 telnet httpbin.org 80
Trying 34.224.230.241...
Connected to httpbin.org.
Escape character is '^]'.
GET /get?username=wccalvin&language=tamil HTTP/1.1
host: httpbin.org

HTTP/1.1 200 OK
Connection: keep-alive
Server: gunicorn/19.9.0
Date: Fri, 24 Aug 2018 02:34:34 GMT
Content-Type: application/json
Content-Length: 247
Access-Control-Allow-Origin: *
Access-Control-Allow-Credentials: true
Via: 1.1 vegur

{
  "args": {
    "language": "tamil",
    "username": "wccalvin"
  },
  "headers": {
    "Connection": "close",
    "Host": "httpbin.org"
  },
  "origin": "100.10.47.251",
  "url": "http://httpbin.org/get?username=wccalvin&language=tamil"
}
```

### Example of a POST request
```console
~ 🔥 telnet httpbin.org 80
Trying 52.207.5.158...
Connected to httpbin.org.
Escape character is '^]'.
POST /post HTTP/1.1
Host: httpbin.org
Content-Length: 32

firstname=xyz&lastname=lmn
```