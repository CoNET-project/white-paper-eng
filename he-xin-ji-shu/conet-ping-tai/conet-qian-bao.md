# CONET錢包

CONET錢包提供類似MetaMask，CoinBase等主流錢包的功能

區塊鏈去中心化應用的CONET錢包，在業界第一次，使用去中心化雲來同步各設備間，同一個12位助記詞帳號下，多個錢包地址的信息更新，讓Web3用戶可享受類似Web2的用戶體驗。

但Web3用戶最關心的是錢包安全，CONET把私鑰最敏感的信息存放在去中心化雲，卻為何比通過物理裝置保護的冷錢包，更具有安全性呢？

數字和物理現實的差別在於，數字可被加密，粉碎，和解密與復原，復原後數字的原價值保持不變，而物理現實被粉碎後，則失去其價值

CONET通過數字特點和加密學，獨創安全錢包新思路

**碎片化，迭代加密，隱私文件名多重機制保護**

CONET把錢包文件拆分為多個碎片，使用[AES-256-GCM](https://juejin.cn/post/6844904122676690951)加密算法，對碎片進行3重迭代加密(三次加密)，再使用HASH算法，產生只有通過助記詞才能恢復的具有隱蔽性的文件名（和錢包地址或私鑰無任何關聯性），加密的碎片隱藏在去中心化存儲的碎片大海洋（目前使用CONET獨創的IPFS兼容去中心化協議）。

```typescript
const SRP: string = ''                                //    Mnemonic Phrase
const currentVer: number = exampleVersion            //    Version number
const root = ethers.Wallet.fromPhrase(SRP)            //    root of account
const FragmentNameWallet = root.deriveChild(65536)    //    connect to no.65536 wallet
const firstVerFileName = ethers.id(FragmentNameWallet.address)    //    hash
const currentVer = '0x' + (BigInt(firstVerFileName) + BigInt(currentVer)).toString(16)
const mainFragmentName = ethers.id( ethers.id( ethers.id(currentVer)))
```

首先從碎片大海洋中，通過無元數據，無關聯的Hash文件名，去揀選某個用戶的錢包文件已經是大海撈針。其次就算拿到了所有碎片，如何按順序完成拼圖，也是一個巨大的挑戰。

再接下來對 [AES-256-GCM加密的文件，進行暴力算法破解](https://www.sdnlab.com/21145.html) 幾乎是不可能，而CONET對碎片進行3次不同密碼的迭代加密，更嚴密防止了被破解。

物理冷錢包，只要拿到它（物理冷錢包有成千上萬的安全漏洞可以偷到它），則等於完成了CONET的大海撈針，也完成了拼湊成一個完整拼圖的工作，所以CONET比物理冷錢包，有著更嚴密的安全性不言而喻。

**受抗暴力破解** [**Scrypt密碼學算法**](https://www.jiamisoft.com/blog/36072-scryptsf.html) **保護的CONET平台本地解鎖**

打開CONET平台，用戶需輸入易記憶的6位簡單密碼，CONET平台通過Scrypt算法，隨機產生一個，可以對抗超級計算機暴力破解的強密碼，來保護本地存儲的已經碎片化的敏感信息

**簡單管理多錢包**

無論是生成的新錢包，還是外部導入的私鑰，一個CONET用戶可以管理成千上萬錢包，每個錢包都可以被標記名稱及顏色。

**助記詞一鍵恢復所有錢包**

只要輸入助記詞，就可從去中心化雲IPFS等，一鍵恢復所有錢包，包括錢包的圖片，名稱和顏色。

**不同設備之間，相同CONET平台帳號同步錢包信息**

手機和電腦可以共享同一個帳戶中的所有錢包信息，並相互之間可同步最新狀態。

**智能化的資產管理**

CONET平台自動掃描主要網絡，搜索帳戶中所有錢包，所有主流網絡中的加密資產，包括NFT資產，無需用戶手工添加。

**全球無障害訪問及具有隱私的鏈上信息交互**

CONET提供高品質，防科學家攻擊的所有主流網絡的私有高速RPC節點，用戶通過CONET Layer Minus無IP地址隱私網絡，可全球無障礙的和所有主流區塊鏈進行安全隱私的交互。

\


\
