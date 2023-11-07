# Burning Credentials Generates

**Requirement**

After users transfer tokens to the designated burning address, then can create burning credentials.

1. Transfer to additional approved Blackhole wallet address.
2. Create burning credentials using the same transfer account number.
3. Include transfer amount, attachment, transfer TX

**Burn/Mint Verify Credentials**

<figure><img src="../../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

**Validators vote to validate note**

1. Get the transfer TX from the block, check the amount consistency, whether the wallet address is consistent with the credential creator, and whether the burning address is an additional specified address.
2. Generate output Hash, check whether it is unique in the Burning/Minting tree (anti-reuse)
3. If the test passes, it will be encrypted and packaged and then inserted into the Burning/Minting tree.
4. The output Hash is a qualified completed transaction.

The user obtains a burnt note hash, which can be prompted when minting later.
