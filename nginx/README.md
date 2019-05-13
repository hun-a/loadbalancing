# How to run?

### Install the module of forever as global

``` 
$ npm i -g forever
```

### Run the app.js by each port

```
$ forever start app.js 8081
$ forever start app.js 8082
$ forever start app.js 8083
$ forever start app.js 8084
```

### Install the Nginx

```
$ brew install nginx
```

### Update the nginx.conf

```
...
http {
  # ...
  upstream nodejs_app {
    server 127.0.0.1:8081;
    server 127.0.0.1:8082;
    server 127.0.0.1:8083;
    server 127.0.0.1:8084;
  }
  #...
  server {
    listen 80;
    location / {
      proxy_pass http://nodejs_app;
    }
  }
  #...
}
...
```

### Restart the Nginx

```
$ nginx -s reload
```

### Connect to `http://localhost`