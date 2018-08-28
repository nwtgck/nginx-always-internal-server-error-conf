# nginx-always-internal-server-error-conf

Nginx configuration to always return "500 Internal Server Error"

## Usage

```bash
docker run -it -p 8081:80 -v $PWD/default.conf:/etc/nginx/conf.d/default.conf nginx
```

Then, you can access to <http://localhost:8081/> and have 500 Internal Server Error page on your browser.

or  

You can use `curl` command.

```bash
$ curl -i localhost:8081
HTTP/1.1 500 Internal Server Error
Server: nginx/1.15.2
Date: Tue, 28 Aug 2018 13:01:45 GMT
Content-Type: text/html
Content-Length: 193
Connection: close

<html>
<head><title>500 Internal Server Error</title></head>
<body bgcolor="white">
<center><h1>500 Internal Server Error</h1></center>
<hr><center>nginx/1.15.2</center>
</body>
</html>
```