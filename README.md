# How to benchmark this app?

### Install the [siege](https://github.com/JoeDog/siege)

``` 
$ brew install siege
```

### Run the below commend to benchmark this app

```
$ siege -c200 -t10s http://localhost:8080
```

### Example

```
Lifting the server siege...
Transactions:		        5017 hits
Availability:		      100.00 %
Elapsed time:		        9.95 secs
Data transferred:	        0.08 MB
Response time:		        0.39 secs
Transaction rate:	      504.22 trans/sec
Throughput:		        0.01 MB/sec
Concurrency:		      194.83
Successful transactions:        5017
Failed transactions:	           0
Longest transaction:	        0.73
Shortest transaction:	        0.01
```