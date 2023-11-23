---
description: >-
  Three major elements of communication: sender address, recipient address, and
  content
---

# Internet TCP/IP Communication Privacy Threats

**Internet TCP/IP Address Privacy Problems**

The TCP/IP package of the Internet communication protocol consists of header metadata including the source address, destination address, and content (data). Due to the widespread use of SSL encrypted communication recommended by [W3C](https://www.w3.org/2001/tag/doc/web-https), the threat of content (data) privacy leakage is greatly reduced.

<figure><img src="../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

Due to the header metadata being transmitted in clear text (unencrypted), personal information about users is leaked:

1. Geographic location of communicating parties
2. Software used to transmit the data
3. Frequency of communication.

Due to ISPs requiring KYC, IANA can obtain a users identity with just the IP address, including the registered owner, and possibly even the current tenant.

Having access to this information makes the internet less open and free.

Packet data can be blocked by IP addresses, on both the sending and the receiving end, preventing users from connecting or making an outbound connections. This data leak can be abused by individual server hosts or even at the ISP level and it is all easily logged.



<mark style="color:red;">webhosts can block users by ip address, preventing specific users or blocking whole regions of users from making connections. In the same way out going communications can be blocked as well.</mark>

<mark style="color:red;">webhosts can deanonymize users that connect to their server</mark>

<mark style="color:red;">webhosts can block certain types of applications</mark>

* <mark style="color:red;">Internet traffic can be filtered based on origin or destination IP address or domain, banning specific users or large groups of users</mark>
* <mark style="color:red;">Block network communication of certain types of applications, such as Bitcoin or torrents</mark>
*

<mark style="color:red;">**Technical measures that network monitors can take**</mark>

* <mark style="color:red;">Traffic filtering system based on destination IP address or domain name.</mark>
* <mark style="color:red;">Obtain the current real geographical location of the monitored object</mark>
* <mark style="color:red;">Obtain the social network of the monitored object.</mark>
* <mark style="color:red;">Block network communication of a certain type of application software. Such as blocking the communication protocol of Bitcoin and Ethereum.</mark>

<mark style="color:red;">**Internet application service providers exploit privacy**</mark>

* <mark style="color:red;">Obtain the visitor’s true identity.</mark>
* <mark style="color:red;">Tailor-made advertising.</mark>
* <mark style="color:red;">Identity-based denial of service.</mark>
* <mark style="color:red;">Record and collect visitor data, combined with big data models, to obtain an accurate personal evaluation system. For example, a centralized artificial intelligence system can evaluate the user's cultural beliefs, knowledge reserves, living habits, IQ level, current happiness, anger, sorrow, and joy through big data analysis based on the accumulation of visitors' questions, and can predict the user's next step. hours, possible actions for the next week.</mark>
