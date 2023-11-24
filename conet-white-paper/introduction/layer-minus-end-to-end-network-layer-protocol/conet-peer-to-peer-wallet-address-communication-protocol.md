---
description: >-
  The wallet address is an unlimited resource created on demand and is the
  unique identifier for communication
---

# CONET peer-to-peer wallet address communication protocol

The CONET wallet address protocol establishes a point-to-point communication mechanism, define how data should be encapsulated, addressed, transmitted, routed, and received at the destination.

<figure><img src="../../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

**Asymmetric Cryptography**

Cryptography contains the following elements:

* Confidentiality: ensuring that information can only be obtained by authorized persons.
* Integrity: Detect whether the message has been tampered with.
* Authentication: The sender and receiver need to be verifiable and identifiable.
* Non-Reputation: Provide transaction proof between the sender and receiver of the message.

Asymmetric encryption allows users to have a pair of keys: a public key and a private key. The "private key" is a random number randomly generated by the computer, including about fifty numbers and sizes. There is no fixed logic or rules for writing letters. The private key and the public key are generated in pairs by calculation and are unique and will not be repeated.

**Wallet Address**

The wallet address is calculated based on the asymmetric encryption "public key" through specific HASH calculation and encoding. Before using the CONET network, users need to create a pair of "public/private key" to distinguish their location on CONET.

Wallet addresses are unlimited resources, created cryptographically by customers on demand, and there is no centralized distribution mechanism.&#x20;

[**Ecrypted with public key**](https://en.wikipedia.org/wiki/Encryption)

In a[ public key encryption system](https://cacr.uwaterloo.ca/hac/about/chap8.pdf), anyone with a public key can encrypt a message and generate ciphertext, but only someone who knows the corresponding private key can decrypt the ciphertext to obtain the original message.

[**Digital signature**](https://en.wikipedia.org/wiki/Digital\_signature)

The sender can use the private key and the message to create a signature. Anyone with the corresponding public key can verify whether the signature matches the message, but a forger who does not know the private key cannot pretend to be the owner of the private key to sign the message. The signature is non-repudiation and played a key role in CONET P2P protocol.

**Leakage of ciphertext side channel information**

Anyone who obtains the ciphertext does not need to decrypt it, and can perform cryptographic calculations on the ciphertext to obtain the public key ID used to encrypt the ciphertext.

**CONET packet**

CONET network data packets do not contain any metadata and are encrypted using the "public key" of the receiving party.

<figure><img src="../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

**CONET nodes**

CONET nodes are the key facilities that make up the CONET wallet routing network. They perform the following tasks

* **Data Relay node**: When a node obtains encrypted data that is not its own agent, node will forward it to the right node that is the agent for the delivery address. Obtain the corresponding traffic fee from the delivery node.
* **Agent receiving node:** Accept the customer's entrustment to receive the encrypted message of the customer's wallet address, and forward the encrypted message to the customer when the entrusted customer is online. Collect usage fees from customers in advance, pay for the data forwarding bandwidth fees forwarded by other nodes on behalf of customers, and deduct them from the prepayment.
* **Data caching in agent receiving node:** The inbound message was storage when the entrusted client is offline.All cached data will be send to client when the client comes online, and the corresponding storage fee is calculated and deducted from the advance payment.
* **SSE in agent receiving node:** When the client connects to the agent receiving node of its own wallet through the network access node through the HTML protocol, the agent receiving node encrypted the incoming data with customer-specified temporary password, then pushes it to the client through [W3C SSE](https://www.w3schools.com/html/html5\_serversentevents.asp) (Server-Sent Events) protocol. Pay the traffic fee to the relay node, charge traffic fee and relay traffic fee from the prepayment.

**Routing**

<figure><img src="../../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

**Traffic Obfuscation Technology**

CONET is a virtual network established using the W3C HTTP protocol at the application layer of  OSI. The CONET communication itself has no characteristics, which is a characteristic of the CONET network.