# Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases: A Design Space Exploration

---

![FDBKeeper Logo](https://github.com/DASE-iDDS/FDBKeeper/blob/main/logo.png)

---

Welcome to FDBKeeper, a scalable coordination service using FoundationDB. We built on top of the [ClickHouse source code repository](https://github.com/ClickHouse/ClickHouse). This is the code repo for the paper "**Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases: A Design Space Exploration**".
The experimental evaluation code is available at [FDBKeeper-Evaluation](https://github.com/DASE-iDDS/FDBKeeper-Evaluation). The code is based on the open-source project ClickHouse and FoundationDB.

## Getting Started with FDBKeeper

### Building on Ubuntu

1. Compiling and installing FDBKeeper from source
```
sudo apt-get update
sudo apt-get install git cmake ccache python3 ninja-build nasm yasm gawk lsb-release wget software-properties-common gnupg
git clone --recursive https://github.com/DASE-iDDS/FDBKeeper
mkdir build
cmake -S . -B build
cmake --build build
```

2. Installing FoundationDB from binary

Developers interested in using FoundationDB can get started by downloading and installing a binary package. Please see the [downloads page](https://github.com/apple/foundationdb/releases) for a list of available packages.




## Core Components of FDBKeeper

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


## Contact
If there are any questions, please feel free to propose new features by opening an issue or contact with the author: Jun-Peng Zhu(zjp.dase@stu.ecnu.edu.cn). Enjoy the code.

