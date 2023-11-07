# Merkel tree

CONET performs all burnable and mintable ledgers via UTXO records stored in the Merkle tree, and ticket operations are operated via burn/mint to prevent double spending.

**Note**

A note can be conceptualized as an owner's banknote. It contains the following records

* Owner's wallet address
* Asset amount
* Asset additional data (supports ERC-3770)
* Burn Voucher Tx

Note Hash

Refers to the hash number calculated by encrypted hashing of the asset additional data of the bill and the burning certificate Tx.

* When a user burns tokens and submits a burning voucher application, and is verified to be qualified, a valid note hash will be obtained.
* When a user mints tokens, a valid note hash is obtained.

**Burning/Minting Merkel Tree**

Record all valid note hashes
