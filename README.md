# blocking-resteasy project

Just a simple standard REST Easy app

## Benchmarks

Warming up
**wrk -t2 -c50 -d30s http://localhost:8080/fruits**
```
Running 30s test @ http://localhost:8080/fruits
  2 threads and 50 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    15.92ms   44.88ms 625.96ms   90.14%
    Req/Sec    23.89k    11.81k   42.95k    58.52%
  1373740 requests in 30.04s, 133.63MB read
Requests/sec:  45732.46
Transfer/sec:      4.45MB
```

Real load:
**wrk -t10 -c200 -d40s http://localhost:8080/fruits**
```
Running 40s test @ http://localhost:8080/fruits
  10 threads and 200 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     8.68ms   28.46ms 624.46ms   95.46%
    Req/Sec     6.17k     1.00k   20.79k    91.08%
  2456363 requests in 40.10s, 238.94MB read
  Socket errors: connect 0, read 142, write 0, timeout 0
Requests/sec:  61256.65
Transfer/sec:      5.96MB
```
