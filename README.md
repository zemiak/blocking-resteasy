# blocking-resteasy project

Just a simple standard REST Easy app

## Benchmarks

Warming up
**wrk -t2 -c50 -d30s http://localhost:8080/fruits**
```
Running 30s test @ http://localhost:8080/fruits
  2 threads and 50 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    13.97ms    5.28ms  83.87ms   85.02%
    Req/Sec     1.83k   138.88     2.04k    88.00%
  108986 requests in 30.01s, 10.60MB read
Requests/sec:   3632.15
Transfer/sec:    361.80KB
```

Real load:
**wrk -t50 -c200 -d40s http://localhost:8080/fruits**
```
Running 30s test @ http://localhost:8080/fruits
  50 threads and 200 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    51.90ms   13.66ms 112.14ms   92.80%
    Req/Sec    76.42     11.00   161.00     73.58%
  114667 requests in 30.10s, 11.15MB read
  Socket errors: connect 0, read 161, write 0, timeout 0
Requests/sec:   3809.27
Transfer/sec:    379.44KB
```
