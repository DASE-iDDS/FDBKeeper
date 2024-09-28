## Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases: A Design Space Exploration

![FDBKeeper Logo](https://github.com/DASE-iDDS/FDBKeeper/blob/main/logo.png)

Welcome to FDBKeeper, a scalable coordination service using FoundationDB. This is the code repo for the paper "**Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases: A Design Space Exploration**".



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


### Contact
If there are any questions, please feel free to propose new features by opening an issue or contact with the author: Jun-Peng Zhu(zjp.dase@stu.ecnu.edu.cn). Enjoy the code.

