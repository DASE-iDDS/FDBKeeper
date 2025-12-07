# FDBKeeper: Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases
---

![FDBKeeper Logo](https://github.com/DASE-iDDS/FDBKeeper/blob/main/logo.png)

---

Welcome to FDBKeeper, a scalable coordination service using FoundationDB. We built on top of the [ClickHouse source code repository](https://github.com/ClickHouse/ClickHouse). This is the code repo for the paper "**FDBKeeper: Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases**" **(Accepted by VLDB 2025)**.
The experimental evaluation code is available at [FDBKeeper-Evaluation](https://github.com/DASE-iDDS/FDBKeeper-Evaluation).

## Getting Started with FDBKeeper

### Building on Ubuntu

We recommend using Ubuntu 22.04.

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

Please see the [downloads page](https://github.com/apple/foundationdb/releases) for a list of available packages.




## The Core Code of FDBKeeper

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

## Citation

Please feel free to cite us if the following papers are helpful.

```bitex
@article{zhu2025fdbkeeper,
  title={FDBKeeper: Enabling Scalable Coordination Services for Metadata Management using Distributed Key-Value Databases},
  author={Zhu, Jun-Peng and Zhang, Lingfeng and Cai, Peng and Zhou, Xuan and Zhao, Peisen and Wang, Xue and Tang, Linpeng},
  journal={Proceedings of the VLDB Endowment},
  volume={18},
  number={12},
  pages={5004--5016},
  year={2025},
  publisher={VLDB Endowment}
}
```
