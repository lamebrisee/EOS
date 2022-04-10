# The name of the game

A valid transaction on the EOSIO blockchain needs to be signed by a "private key".

The signature to be done will require a specific "permission".**

This permission will be held by an account

This may be an over simplification but it helps to get the concepts and big picture.

NOTE: with EOS we need to already have an account to create a new one.
---
      this is why we are using the already available account default "eosio" on every chain
      we are using the eosio account on the Development environment.

# 1)Creating an account inside a wallet

cleos create account eosio [accountNameHere] [ownerKey] [activeKey]

example:

cleos create account eosio alice 5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3

NOTE: 5KQwrPbwd....kvFD3 is the owner key for the eosio account

you should see a confirmation message to the following for each command that confirms that the transaction has been broadcast:

executed transaction: 40c605006de...  200 bytes  153 us
         eosio <= eosio::newaccount            {"creator":"eosio","name":"alice","owner":{"threshold":1,"keys":[{"key":"EOS5rti4LTL53xptjgQBXv9HxyU...
warning: transaction executed locally, but may not be confirmed by the network yet    ]

get account info

cleos get account [accountNameHere]
example: cleos get account alice

You should see a message similar to the following:

permissions:
     owner     1:    1 EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV
     
        active     1:    1 EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV
        
memory:
     quota:       unlimited  used:      3.758 KiB

net bandwidth:
     used:               unlimited
     available:          unlimited
     limit:              unlimited

cpu bandwidth:
     used:               unlimited
     available:          unlimited
     limit:              unlimited

Note : EOS6MRyAjQq8ud7hVNYcfnVPJqcVpscN5So8BhtHuGYqET5GDW5CV / 5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3
this is the public/private key pair for the eosio user on the Develpement environment.
