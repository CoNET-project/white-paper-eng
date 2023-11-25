---
description: 為次世代應運而生的新互聯網通訊協議
---

# Layer Minus通訊協議

Layer Minus協議，建立了以錢包地址，作為設備區分彼此的唯一標識，進行點對點通訊的網絡協議，將數據應該如何封裝、定址、傳輸、路由以及在目的地如何接收。

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

**非對稱加密學**

密碼學(Cryptography)包含以下元素：

* 機密性(Confidentiality)：確保訊息只有被授權者才能取得
* 完整性(Integrity)：偵測訊息是否遭受竄改
* 身分認證(Authentication)：傳送方與接受方需驗證識別
* 不可否認性(Non-Reputation)：提供訊息傳送方與接受方的交易證明

非對稱式加密就是每個使用者都擁有一對金鑰：公開金鑰(Public key)及私密金鑰(Private key)「私鑰」是一段由電腦隨機產生的亂數，包含了大約五十個數字和大小寫字母， 沒有固定的邏輯和規則。私鑰與公鑰是成對由計算生成，具有唯一性不會重複。

**錢包地址**

錢包地址是根據非對稱加密的「公鑰」經過特定HASH計算及編碼推算而成。用戶在使用CONET網絡之前，需要自行創建一對「公鑰-私鑰」及錢包地址，用來區分在CONET上的位置。

錢包地址是無限資源，由客戶按需創建，不存在中心化的分配機制。

**公鑰加密**

在[公鑰加密系統中](https://cacr.uwaterloo.ca/hac/about/chap8.pdf)，任何擁有公鑰的人都可以[加密](https://en.wikipedia.org/wiki/Encryption)訊息，產生密文，但只有那些知道相應私鑰的人才能解密密文以獲取原始訊息。

**非對稱加密學**[**數字簽名**](https://en.wikipedia.org/wiki/Digital\_signature)

發件人可以使用私鑰和訊息來建立簽名。任何擁有相應公鑰的人，都可以驗證簽名是否與訊息匹配，但不知道私鑰的偽造者，無法冒充私鑰擁有者對訊息進行簽名，簽名具有[不可否認](https://en.wikipedia.org/wiki/Non-repudiation)，在CONET錢包地址點對點網絡中起到了關鍵作用。

**密文的側通道信息洩漏**

獲得密文的任何人無需解密，對密文進行加密學計算，可獲得加密該密文所使用的公鑰ID。

**Layer Minus 網絡數據包**

Layer Minus網絡數據包，不包含任何元數據，使用接受信息方的「公鑰」進行加密後的數據包。

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**Layer Minus節點**

節點是組成Layer Minus錢包路由網的關鍵設施，它們執行以下任務

* **節點間數據傳遞：**當一個節點獲得非自己代理的加密數據時，會轉發該加密數據到送達節點，送達節點則支付相應的流量費。
* **代理收件人：**節點接受客戶委託，代理客戶接受該錢包地址的加密信息，當該委託客戶在線時，轉發加密信息到該客戶。預收客戶支付使用費用，代客戶支付其他節點轉發過來的數據轉發帶寬費用，並在預付款中扣除。
* **代理收件人的數據緩存：**節點接受客戶委託，代理客戶接受該錢包地址加密信息，當該委託客戶離線時，緩存該加密信息，等下一次委託客戶上線後，發送所有緩存加密信息，計算相應的存儲費用，在預付款中扣除。
* **在線客戶端數據送達：**客戶端通過HTML協議經過入網節點，連結到自己錢包的代理收件人節點後，代理收件人可通過HTML的SSE(Server-Sent Events)通訊協議，向客戶端推送進入的數據包。

**路由**

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**流量混淆**

Layer Minus是在網絡通訊OSI的應用層使用W3C的HTTP協議建立的虛擬網絡，Layer Minus通訊本身沒有任何特徵，是Layer Minus網絡的特點。
