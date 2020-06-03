# fuzzing

Now we start using fuzzing to help us find more bugs. And fuzzing has proven to be a very effective way to find bugs.

In PingCAP, we using fuzzing for many years. At first, we start using [go-randgen](https://github.com/pingcap/go-randgen) to generate random SQL to do differential testing.

And we also rewrite sqlsmith, the project is in tipocket and the name is [go-sqlsmith](https://github.com/pingcap/tipocket/tree/master/pkg/go-sqlsmith). Both go-randgen and go-sqlsmith is useful to do differential testing.

Since TiDB is not 100% compatibility with MySQL. The correctness is still hard to cover, then we use a go version of [sqlancer](https://github.com/sqlancer/sqlancer). The original one has proven to be a very effective way to find correctness bugs in https://www.manuelrigger.at/dbms-bugs/

In the TiDB cluster, we have hundreds of configs, we also need to test if each config is work well on common tests and on fuzz tests. So we create a project [matrix](https://github.com/chaos-mesh/matrix)