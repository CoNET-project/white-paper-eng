# Minting operation UTXO

User can perform casting operations by operating the note hash.

**Minter operation**

It performs a UTXO by hashing one/two input note and creating two new output note. Follow these rules

1. The sum of input note assets equals the output.
2. Entered note are on the Burning/Minting tree.
3. Owner: The wallet specified by the additional.
4. Destination: Specified by owner.

<figure><img src="../../../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

**Validators vote to validate note**

1. Verify that the sum of the outputs equals the inputs.
2. The minted note owner address is additionally specified.

Then output the Hash is a qualified completed transaction.

To better understand what this means, let's consider some practical examples.

**Remint tokens**

The ERC20 contract address then mints new tokens, and appends ERC-3770, which can be other chain information, to realize cross-chain information transfer. The owner's wallet with the right to re-mint mints new tokens to the owner's designated address, then signs and attaches the transfer voucher Tx give the minter the right to use the note. Then the note cannot be reused.



**Validators vote to validate note**

1. Verify that the sum of the outputs equals the inputs.
2. Verify successful transfer TX information.
3. Verify owner wallet address.
4. Verify attachments are consistent.

Then output the Hash is a qualified completed transaction.
