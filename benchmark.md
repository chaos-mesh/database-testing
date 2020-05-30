In PingCAP. We build a platform and many tools for benchmarking. The platform contains many standerd bencmarking(such as TPCC/TPCH/YCSB/SYSBENCH).

The platform is [here](http://perf.pingcap.com)
![Benchmark](./static/benchmark_overview.png )
We also implement many tools for benchmark. First of all is go-tpc(Now it can run tpcc and tpch)
Yes, why we implement it is because benchmarksql is hard to use and we want make the usage much easy. And we also improve the speed of generat data much(about 3-10x faster then benchmarksql)