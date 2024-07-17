<meta name="robots" content="noindex">
## FDBKeeper

This is the code repo for paper: **Enabling Scalable Coordination Services using Distributed Key-Value Databases: A Design Space Exploration**. submitted to SIGMOD 2025



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
