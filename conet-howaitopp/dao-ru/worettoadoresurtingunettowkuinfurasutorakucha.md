---
description: インターネット層のプライバシー ソリューション
---

# ウォレットアドレスルーティングネットワークインフラストラクチャ

インターネットはハードウェア インフラとソフトウェア インフラで構成されます。 ハードウェア インフラは、コンピュータ、ワイヤレス ルーター、および重要な[インターネット インフラ](https://www.ieice.org/\~cs-edit/magazine/ieice/spsec/Bplus9\_sp.pdf) ([ワイヤレス ルーター](https://www.gate02.ne.jp/media/it/column\_44/)、[ISP アクセス ハブ](https://www.pken.com/school/materials/pdf/kadai\_h\_02.pdf)、[光ファイバー ケーブル](https://ja.wikipedia.org/wiki/%E5%85%89%E3%82%B1%E3%83%BC%E3%83%96%E3%83%AB)、[スイッチ](https://medium-company.com/%E3%83%8F%E3%83%96-%E3%83%AA%E3%83%94%E3%83%BC%E3%82%BF-%E3%83%96%E3%83%AA%E3%83%83%E3%82%B8-%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81%E3%81%AE%E9%81%95%E3%81%84/)、[バックボーン回線](https://www.idcf.jp/words/backbone.html) [ネットワークの衛星](https://xtech.nikkei.com/atcl/nxt/mag/nnw/18/091900032/061700046/)および[海底ケーブル](https://www.nikkei.com/topics/22A00457)など) で構成されます。 ソフトウェアインフラは、[通信プロトコル](https://ja.wikipedia.org/wiki/Internet\_Protocol)、[ドメインネームシステム](https://ja.wikipedia.org/wiki/Domain\_Name\_System)、ログインシステム、[データセンター](https://ja.wikipedia.org/wiki/%E3%83%87%E3%83%BC%E3%82%BF%E3%82%BB%E3%83%B3%E3%82%BF%E3%83%BC)などで構成されます。

重要なインターネットインフラの構築には巨額の設備投資が必要となるため、これらの機器の所有権は独占企業や国家の手に集中しています。 同時に、IPアドレスの割り当て、通信プロトコルの策定、ドメイン名解釈ルートサーバーなど、インターネット通信のための主要なソフトウェアインフラストラクチャも独占企業によって所有されています。

[OSI参照モデル](https://ja.wikipedia.org/wiki/OSI%E5%8F%82%E7%85%A7%E3%83%A2%E3%83%87%E3%83%AB)

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

通信システムのデータフローは、分散アプリケーション ータの最上位レベルの表現から、通信メディアを介したデータ送信の物理的な実装まで、7 つの層に分割されます。 物理層には、すべての重要なハードウェア インフラを指します。 データリンク層以降はすべてソフトウェアスコープであり、各中間層はその上の層に機能を提供し、その下の層が独自の機能を提供します。機能カテゴリは、標準の通信プロトコルを通じてソフトウェアに実装されます。

[コンピュータのネットワーク](https://ja.wikipedia.org/wiki/%E3%82%B3%E3%83%B3%E3%83%94%E3%83%A5%E3%83%BC%E3%82%BF%E3%83%8D%E3%83%83%E3%83%88%E3%83%AF%E3%83%BC%E3%82%AF)標準策定に主要な役割を果たしている 2 つの主要な国際組織は、[国際電気通信連合](https://ja.wikipedia.org/wiki/%E5%9B%BD%E9%9A%9B%E9%9B%BB%E6%B0%97%E9%80%9A%E4%BF%A1%E9%80%A3%E5%90%88%E9%9B%BB%E6%B0%97%E9%80%9A%E4%BF%A1%E6%A8%99%E6%BA%96%E5%8C%96%E9%83%A8%E9%96%80)の電気通信標準化部門と[国際標準化機構 (ISO) ](https://ja.wikipedia.org/wiki/%E5%9B%BD%E9%9A%9B%E6%A8%99%E6%BA%96%E5%8C%96%E6%A9%9F%E6%A7%8B)です。これらの標準により、世界中のさまざまなタイプやオペレーティング システムのコンピュータがお互いに通信ができるようになります。
