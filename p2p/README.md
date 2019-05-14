# How to run

#### Start app instance as twice

```
$ node app.js 8081
$ node app.js 8082
```

#### Start the client.js

```
$ node client.js
```

##### result

- app.js 8081

```
Started 25288
Handling request from 25288
Handling request from 25288
Handling request from 25288
Handling request from 25288
Handling request from 25288
```

- app.js 8082

```
Started 25294
Handling request from 25294
Handling request from 25294
Handling request from 25294
Handling request from 25294
Handling request from 25294
Handling request from 25294
```

- client.js

```
Hello from 25294

Hello from 25288

Hello from 25294

Hello from 25288

Hello from 25294

Hello from 25288

Hello from 25294

Hello from 25288

Hello from 25294

Hello from 25288

Hello from 25294
```