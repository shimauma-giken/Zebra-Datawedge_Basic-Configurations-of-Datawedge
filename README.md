## Zebra DataWedgeの基本設定 (初めての方向け）

----
<br/>

### DataWedgeとは？

<img src="https://www.zebra.com/content/dam/zebra_dam/global/photography/application/0002/handhelds-landing-page-full-width-image.jpg.imgo.jpg">

DataWedgeはZebraのAndroidデバイスに搭載されているアプリケーションサービスで、スキャナやRFIDを含む入力データを効率的にアプリケーションと連携するためのものとなります。

DataWedgeを使用することで、スキャナなどからのデータ入力に関するコーディングを大幅に削減することができるようになります。

このサービスは、バーコードスキャナ、マグストライプリーダー（MSR）、RFID、音声入力、シリアルポートなど、複数の入力ソースからデータを取得し、必要に応じてそのデータをフォーマットすることができます。


本頁ではDataWedgeの基本的な機能について説明をします。

<br/>


##### 参考リンク
[DataWedge 11.3 - 概要](https://techdocs.zebra.com/datawedge/dw-jp/11-3/guide/about/)

---

### 特定のアプリ向けのDataWedgeプロファイルを作成する方法

<img height="500" src="image/sample/1742640676924.png">

スキャンデータなどの入力データをアプリケーション毎に設定をしたいケースがあります。

#### 例、
- アプリAではスキャン後にエンターキーを付与したい
- アプリBではスキャン後にタブキーを付与したい

このような要望に答えるため、アプリケーション毎に専用設定（プロファイル）を作成する機能がDataWedgeにはあります。

プロファイルの詳細や作成方法は下記リンクを参照ください。

<br/>


##### 参考リンク
[サードパーティ アプリケーション用の DataWedge プロファイルの作成](https://supportcommunity.zebra.com/s/article/Creating-a-DataWedge-profile-for-a-third-party-application?language=ja)

---
### 読み取り対象のバーコードを設定

<img height="500" src="./image/sample/1742640794038.png">

DataWedgeにおいてはスキャン対象のバーコードタイプを取捨選択することができます。読み取り範囲に多くのバーコードが密集しており、特定タイプのバーコードのみを選択したい場合などに活用される設定項目となります。

<br/>


#### 設定方法

1. DataWedgeを起動 > [設定対象のプロファイル] を選択します。
1. "バーコード入力"カテゴリ >  スキャナ設定 >  デコーダー 
1. スキャン対象のバーコードタイプのみ選択された状態とします。
<br/>



    設定例：EAN13 (JANコード/13,8桁)の選択
    <img height="500" src="./image/sample/1742635884259.png">
<br/>


1. 上記設定により、選択したバーコードタイプのスキャンデータのみ読み取るようになります。
<br/>


    スキャン例：
    <img height="500" src="image/sample/1742636014574.png">

<br/>


##### 参考リンク
[DataWedge 11.0 - デコーダ](https://techdocs.zebra.com/datawedge/dw-jp/11-0/guide/decoders/)

---

### スキャンデータの前後にデータを付与する設定

DataWedgeにおいてはスキャンデータの前後に任意のデータを付与することができます。一般的には下記のような用途でよく用いられます。

- スキャンデータの後にエンターキー(CRLF)を付与
- スキャンデータの後にタブキー(TAB)を付与

下記の説明ではスキャンデータの後にエンターキーを付与する設定について説明をします。

#### 設定方法

1. DataWedgeを起動 > [設定対象のプロファイル] を選択します。
1. "キーストローク"カテゴリ >  基本データフォーマット 
1. "Enter キー送信"を選択します。
<br/>


    設定例：エンターキーを付与
    <img height="500" src="image/sample/1742636545489.png">
<br/>



1. テキストエディタ等でスキャン後にEnterキーが追加されていることが確認できます。

    4901085647202をスキャンした例：
    <img height="500" src="image/sample/1742637026818.png">
<br/>


##### 参考リンク
[DataWedge 11.0 - 基本データ形式](https://techdocs.zebra.com/datawedge/dw-jp/11-0/guide/process/bdf/)

---

#### より高度なデータ付与設定方法

スキャンデータにより高度なプリフィックスやサフィックスを追加したい場合は下記に従って設定をお願いいたします。

1. DataWedgeを起動 > [設定対象のプロファイル] を選択します。
1. "キーストローク"カテゴリ >  高度なデータフォーマット（ADF）

<br/>


##### 参考リンク
[DataWedge 11.0 - ADF](https://techdocs.zebra.com/datawedge/dw-jp/11-0/guide/process/adf/）

---

### その他の設定について

上記記載以外にもDataWedgeでは多くの設定ができます。より高度なデータ加工方法についてはTechDocsを参照いただけますと幸いです。

<br/>


##### 参考リンク
[DataWedge 11.3 - 概要](https://techdocs.zebra.com/datawedge/dw-jp/11-3/guide/about/)
