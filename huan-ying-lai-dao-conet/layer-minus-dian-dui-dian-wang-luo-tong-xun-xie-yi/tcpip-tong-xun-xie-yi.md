---
description: 計算機通過唯一識別TCP/IP地址進行通訊
---

# TCP/IP通訊協議

[TCP/IP](https://zh.wikipedia.org/wiki/TCP/IP%E5%8D%8F%E8%AE%AE%E6%97%8F)提供了點對點連結的機制，將資料應該如何封裝、定址、傳輸、路由以及在目的地如何接收，都加以標準化。

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

[**IP地址**](https://en.wikipedia.org/wiki/IP\_address)

當設備連接網絡，設備將被分配一個IP位址，用作唯一標識。 透過IP位址，設備間可以互相通訊，如果沒有IP位址，我們將無法知道哪個設備是發送方，無法知道哪個是接收方。 IP位址有兩個主要功能：標識設備或網路和定址。

1981年，[IETF](https://www.ietf.org/)定義了32位元IP位址的[IPv4](https://zh.wikipedia.org/wiki/IPv4)，隨著網際網路的發展，IPv4漸漸被消耗殆盡。其升級版[IPv6](https://zh.wikipedia.org/wiki/IPv6)在1998年12月由[互聯網工程工作小組](https://zh.wikipedia.org/zh-hant/%E4%BA%92%E8%81%94%E7%BD%91%E5%B7%A5%E7%A8%8B%E4%BB%BB%E5%8A%A1%E7%BB%84)以互聯網標準規範（[RFC 2460](https://datatracker.ietf.org/doc/html/rfc2460)）的方式正式公佈。

**IP地址空間分配**

IP位址空間無論是IPv4和IPv6，都是由中心化的[網路號碼分配局](https://zh.wikipedia.org/wiki/%E4%BA%92%E8%81%94%E7%BD%91%E5%8F%B7%E7%A0%81%E5%88%86%E9%85%8D%E5%B1%80)，在全球範圍進行分配（英文：Internet Assigned Numbers Authority，簡稱：[IANA](https://en.wikipedia.org/wiki/Internet\_Assigned\_Numbers\_Authority)）以及其他5個區域[網路註冊管理機構](https://zh.wikipedia.org/wiki/%E5%8C%BA%E5%9F%9F%E4%BA%92%E8%81%94%E7%BD%91%E6%B3%A8%E5%86%8C%E7%AE%A1%E7%90%86%E6%9C%BA%E6%9E%84)（英文：Regional Internet Registry，簡稱：[RIR](https://en.wikipedia.org/wiki/Regional\_Internet\_registry)）在其指定區域內分配給互聯網。

**IP地址租賃**

用戶使用互聯網時，需要向[互聯網服務供應商](https://zh.wikipedia.org/wiki/%E4%BA%92%E8%81%94%E7%BD%91%E6%9C%8D%E5%8A%A1%E4%BE%9B%E5%BA%94%E5%95%86)完成[KYC](https://zh.wikipedia.org/wiki/%E8%AA%8D%E8%AD%98%E4%BD%A0%E7%9A%84%E5%AE%A2%E6%88%B6)(認識客戶)手續後，才能租賃一個全球唯一IP地址。

[**路由**](https://zh.wikipedia.org/wiki/%E8%B7%AF%E7%94%B1)

由於互聯網結構複雜，兩台電腦之間如何發現彼此，尋找一個合適的最佳路徑。[路由器](https://zh.wikipedia.org/wiki/%E8%B7%AF%E7%94%B1%E5%99%A8)是決定如何把一個[IP數據包](https://zh.wikipedia.org/wiki/%E7%B6%B2%E8%B7%AF%E5%B0%81%E5%8C%85)轉送出去，在互聯網上相互連結的關鍵設施。 IP包可以途徑多個路由，但不保證能到達，也不保證順序到達。

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

**虛擬隧道概念**

通過分層概念，互聯網通訊可以被簡化為，主機到主機的網絡通訊，應用程式到應用程式的網絡通訊。
