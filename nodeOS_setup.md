# Nodeos EOSIO server Setup Guide

This file describes the process i follow to setup/install a nodeos EOSIO server client on ubuntu 18.04.

## Getting Started

Step 1: Install binaries
* [EOSIO](https://github.com/EOSIO/eos/releases/). -EOSIO client
```
wget https://github.com/EOSIO/eos/releases/download/v2.0.4/eosio_2.0.4-1-ubuntu-18.04_amd64.deb
sudo apt install ~/eosio_2.0.4-1-ubuntu-18.04_amd64.deb
```
* [CDT](https://github.com/EOSIO/eosio.cdt/releases/). -EOSIO cdt client

Step 2: Install CDT
```
wget https://github.com/EOSIO/eosio.cdt/releases/download/v1.7.0-rc1/eosio.cdt_1.7.0-rc1-ubuntu-18.04_amd64.deb
sudo apt install ~/eosio.cdt_1.7.0-rc1-ubuntu-18.04_amd64.deb
```

Step 3: Setup Directory
```
mkdir contracts
```
