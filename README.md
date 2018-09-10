Node Build
This install works for Ubuntu 16.04 (CLEAN OS)

1. Make directory for install and cd to the directory, make sure the user has SUDO
FYI: https://www.digitalocean.com/community/tutorials/how-to-create-a-sudo-user-on-ubuntu-quickstart

2. Login as the new user (if not so already -- no not recommend using root user).

2. Make sure you have dependencies:

sudo apt-get install -y build-essential python-dev gcc g++ git cmake libboost-all-dev

3. Recommend nano for editing: 

sudo apt-get install nano

4. Make sure you have GIT: 

sudo apt-get install git

5. Git the package

git clone https://github.com/hashratez/everycash.git

6.From your directory

mkdir build

cd build

cmake ..

make



```
// Copyright (c) 2012-2017, The CryptoNote developers, The Bytecoin developers
// Copyright (c) 2014-2018, The Monero Project
// Copyright (c) 2018, The TurtleCoin Developers
// 
// Please see the included LICENSE file for more information.
```
