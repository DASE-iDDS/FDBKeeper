## FDBKeeper

This is the code repo for paper: **Enabling Scalable Coordination Services using Distributed Key-Value Databases: A Design Space Exploration**。
We demonstrate how to design and implement key features of coordination services in FoundationDB, known as FDBKeeper (approximately 7k
lines of code). We have successfully replaced ZooKeeper (about 200k lines of code) with FDBKeeper in the ClickHouse deployment
and demonstrated that it has better performance and scalability in a production environment. 


### Modification Lists

* src (Core Modification)
  * src/Common/FoundationDB
  * src/Interpreters/Context.cpp
* programs
  * programs/keeper-client/KeeperClient.cpp
  * programs/keeper-client/Commands.cpp
  * programs/keeper/CMakeLists.txt
  * programs/server/Server.cpp
* CMakeLists.txt adds FDB compilation options
* contrib/fdb-c-cmake
* tests
  * tests/clickhouse-test
  * tests/config/config.d/fdbkeeper.xml
  * tests/config/install.sh
  * tests/integration/
  * tests/queries
* utils
  * utils/keeper-bench
  * utils/check-style
