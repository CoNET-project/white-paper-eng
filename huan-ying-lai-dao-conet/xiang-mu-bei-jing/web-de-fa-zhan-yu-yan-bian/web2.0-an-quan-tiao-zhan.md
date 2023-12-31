# Web2.0安全挑戰

現今的web2.0應用程式是開放存取和動態產生的，web2.0的這個特性變得更有趣但也帶來了更大的安全風險。

例如，使用者/駭客可能會上傳內容，這些內容可以運行程式碼或攜帶惡意軟體來執行一些惡意任務。 有時駭客可能會將免費防毒軟體之類的軟體上傳到facebook等社交網站（現在人們對facebook或其他社交網站過於沉迷，用戶盲目點擊每個鏈接，每個應用程式和駭客都會利用這一愚蠢的點 ）或任何其他應該是病毒清除軟體但加載特洛伊木馬的網站。 駭客可能會上傳有害程式碼，其中可能包括捕獲受害者擊鍵的鍵盤記錄器——包括受害者的信用卡資訊、密碼並將其發送回給駭客。

**常見的 Web2.0漏洞**

Web 2.0有很多漏洞，其中一些在下面列出：

* 跨站點腳本&#x20;
* 跨站點請求偽造
* SQL注入
* 認證和授權缺陷
* 資訊外洩

**跨站腳本 (XSS)**

在XSS攻擊中，駭客將自己的可執行程式碼注入到合法的、動態產生的網頁中。 每當有人造訪或下載該特定網頁時，駐留在網頁內的程式碼就會在受害者的電腦上執行，並為駭客控制受害者的電腦提供了一條途徑。

**跨站請求偽造 (CSRF)**

在CSRF攻擊中，駭客使用受害者的IP位址或cookie來取得存取權限或繞過防火牆保護造訪受害者已造訪的電子商務、公司內部網路或其他網站 /認證。 這使駭客能夠充當電腦所有者並執行有害行為，例如從個人銀行帳戶中提取資金、從電子商務網站購買東西、從公司內部網路竊取資料或更改路由器或本地防火牆的配置。

**SQL注入**

在SQL注入中，駭客透過從客戶端插入應用程式的輸入資料或「注入」他自己的SQL查詢。 攻擊者不僅可以存取客戶端 Web 應用程式和資料庫，還取決於攻擊者可以存取作業系統的資料庫。 在Xpath注入中，攻擊者更改XML查詢以實現其目標。 當客戶端向網站提供輸入時，會為XML資料建立Xpath查詢，因此攻擊者可以故意發送一些資料以了解XML資料的結構或存取他通常無法存取的資料。 在JSON注入中，攻擊者將惡意JavaScript程式碼注入客戶端網站的JSON中，當用戶端以經過驗證的使用者身分登入目標網站（攻擊者想要入侵的網站）時，攻擊者會向受害者傳送 連結並說服她訪問受感染的網站（由駭客創建的網站）。 如果用戶端在她已經登入目標站點時造訪了受感染的站點，則該目標站點中存在的所有資訊都會傳送給駭客。

**XSS Worms**

駭客將自我傳播的XSS程式碼注入到網頁/應用程式中，這些程式碼將在使用者造訪該頁面時傳播。

**混搭**

混搭背後的主要想法是將來自多個網站的所有資源或服務組合到單一的使用者體驗中。 它可以動態連接到不一定在提供者控制下的網站，這對內容提供者來說是一個安全風險。

**身份驗證和授權缺陷**

身份驗證和授權技術存在各種弱點，例如密碼沒有最大年齡限制，有時密碼長度和複雜性是固定的，密碼可以被猜測（缺乏暴力保護），會話ID可以預見，在大多數情況下，會話ID 的逾時和生命週期沒有時間限制，整個會話只使用一個ID，驗證碼系統中使用的字元或數字被破壞。

**信息泄漏**

有时应用程序会无意中泄漏有关其内部工作、配置的信息，例如通过在URL上添加一些小改动，我们每次都可以得到多个信息。 例如“http://www.mywebsites.com/home.html”而不是“home.html”，如果我们尝试“admin.html”（它应该不存在于网站界面中），有时它可能会显示该特定页面（如果它存在于服务器中）。

