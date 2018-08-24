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
