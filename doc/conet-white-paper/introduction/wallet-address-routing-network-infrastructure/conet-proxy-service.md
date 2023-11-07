---
description: The edge of privacy
---

# CONET Proxy Service

**Introduction**

CONET proxy is a commercial application based on the decentralized zero-trust, privacy-first CONET wallet address routing network.

Proxy service is one of the commonly used applications on the Internet. It can help customers hide their real IP addresses and let the proxy server access Internet websites on their behalf as a way to gain privacy. Many applications natively support the use of proxy servers, such as Firefox, Telegram, Game applications, etc. The traditional proxy server is remote, and customers access the proxy through the Internet.

<figure><img src="../../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

**Traditional proxy service structure**

1. **Traffic receiving layer**-receives traffic from clients accessing the Internet.
2. **Proxy protocol layer** - responds to different proxy protocols used by clients.
3. **Proxy access client** - sends Internet access request to the target server on behalf of the client, then back the response from server to the client.

**CONET proxy service structure**

CONET splits the proxy server into two parts.

1. **Client's local side**: Receives the client's network access traffic, then packages it into a CONET network package, then sends it to the CONET privacy network to connects to the proxy server through the wallet address.
2. **Remote part**: After receiving the client request flowing in through the wallet address, the proxy server uses its own IP address to access the target server on behalf of the client, then back the responds from target server to the client.

**CONET proxy service features**

**Fragmented Traffic**

<figure><img src="../../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

When opens the Google homepage, you can see that the entire homepage is composed of 42 different types of files. The CONET proxy service can use 42 different nodes in the CONET network to process these 42 different requests at the same time, proxy the client to make Google requests.

From the view of Google, it cannot imagine that 42 requests from different IP addresses are issued from the same browser page. From the perspective of network monitors, customers are visiting multiple different websites, which can confuse the monitors' big data analysis. It is also impossible for the participants nodes within CONET to piece together traces of customers’ network access.

**Traffic obfuscation technology**

Benefit from the traffic obfuscation technology of the CONET wallet address network, the CONET proxy service hides the obvious fingerprints of proxy service communications, making it impossible for network monitors to identify that client are using VPN for private communications. CONET proxies can be used to bypass network blocking techniques.
