# Benchmark
In PingCAP. We build a platform and many tools for benchmarking. The platform contains many standerd bencmarking(such as TPCC/TPCH/YCSB/SYSBENCH). And run day by day.

## Benchmark Platform
The platform is [here](http://perf.pingcap.com)
![Benchmark](./static/benchmark_overview.png )

## Benchmark Tools
- [go-tpc](https://github.com/pingcap/go-tpc). We implement it to simplify to run TPCC and TPCH (for load data about 3-10x faster then benchmarksql and much easy to use). You can just using the following steps
    - 1 `./bin/go-tpc -H 127.0.0.1 -P 3306 -D tpcc tpcc --warehouses 4 prepare` to prepare
    - 2 `./bin/go-tpc  -H 127.0.0.1 -P 3306 -D tpcc tpcc --warehouses 4 check` to check
    - 3 `./bin/go-tpc  -H 127.0.0.1 -P 3306 -D tpcc tpcc --warehouses 4 run` to run
- [go-ycsb](https://github.com/pingcap/go-ycsb). We implement it to simplify the usage of ycsb. It is also very easy to use.