# EOSIO CLI commands

Some stuffs to copy/paste in future for CLEOS node on LINUX.

## Creating wallet

creating a wallet with personal name, will print password in console, KEEP PASSWORD SAFE.
```
cleos wallet create -n [namehere] --to-console
```
## Creating eosio keys to later import on a wallet.
creating keys (public and private) to used on a wallet. Can create as many as you need. KEEP PRIVATE KEYS SAFE.
cleos create key --to-console
```
After, private keys must be imported into a wallet.
IMPORTANT: private keys to create account must be imported into the wallet. THIS IS A PUBLIC PRIVATE KEY, CAN BE FOUND ON INTERNET.
5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3
```
cleos wallet import
```
paste private key.
to check private keys on a wallet
```
cleos wallet private_keys
```
it will show all public and private keys managed by the wallet.

## Creating an account inside a wallet.
After properly wallet created and imported with eosio private keys (to create accounts) and his own private key.
```
cleos create account eosio [accountNameHere] [ownerKey] [activeKey]
```
get account info
```
cleos get account [accountNameHere]

## Compilation
---
eosio-cpp -abigen -o dogcontract.wasm src/dogcontract.cpp
```
eosio-cpp -abigen -o dogcontract.wasm src/dogcontract.cpp
--




