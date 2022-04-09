EOSIO CLI commands (LINUX)

Misconception about WALLETS:

A common misconception in cryptocurrency regarding wallets is that they store tokens.
However, in reality, a wallet is used to store private keys in an encrypted file to sign transactions.
Wallets do not serve as a storage medium for tokens.

The name of the GAME 
Creating a wallet which will contaim keys pairs (public/private) used by an account to sign transactions on the blockchain.

NOTE: with ETHEREUM a Smart Contract is deployed to an adress

      with EOS it is deployed by an account    

1)Creating wallet

2)Open the Wallet

3)Unlock a Wallet

4)Creating "eosio user" keys to later import on a wallet

5)Import the Development Key

1)Creating wallet
creating a wallet with personal name, will print password in console, KEEP PASSWORD SAFE
This will help later to unlock the Wallet

cleos wallet create -n [namehere] --to-console

2)Open the Wallet
Wallets are closed by default when starting a keosd instance, to begin, run the following

cleos wallet open

cleos wallet list

and it will return

Wallets:
[
  "default"
]

3)Unlock a Wallet
The keosd wallet(s) have been opened, but is still locked
at step 1) you were provided a password, you're going to need that now.

cleos wallet unlock
Enter the passwd

cleos wallet list 

Wallets:
[
  "default *"
]

NOTE : Pay special attention to the asterisk (*). This means that the wallet is currently unlocked

4)Creating eosio keys to later import on a wallet.
creating keys (public and private) to used on a wallet. Can create has many as you need. KEEP PRIVATE KEYS SAFE

cleos create key --to-console

Afterwards private keys must be imported into a wallet.

5)Import the Development Key
Every new EOSIO chain has a default "system" user called "eosio".
This account is used to setup the chain by loading system contracts that dictate the governance and consensus of the EOSIO chain.
Every new EOSIO chain comes with a development key, and this key is the SAME !!
Load this key to sign transactions on behalf of the system user (eosio)

cleos wallet import

You'll be prompted for a private key, enter the eosio development key provided below:

5KQwrPbwdL6PhXujxW37FSSQZ1JiwsST4cqQzDeyXtP79zkvFD3

THIS PUBLIC PRIVATE KEY SHOULD NEVER BE USED FOR PRODUCTION !! 


