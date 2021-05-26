# WCH_BasicK

<img src="https://github.com/akita11/WCH_BasicK/blob/master/WCH_BasicK.jpg" width="400px">

## これは何？

- [中国のWCH社](http://www.wch-ic.com/)の格安USB-シリアル変換チップCH340Kを使った、USB-シリアル変換器です。
- Arduino等の書き込みやシリアル通信で、標準的に使われる[FTDI Basic](https://www.switch-science.com/catalog/342/)と同じ6ピンコネクタを備えています。
- PC側のコネクタはUSB Type-Cです。
- FTDI Basic互換の6ピンコネクタ以外に、ESP32の書き込み等で用いられるRTS#信号を、脇の端子に引き出してありますので、必要な場合はそこにコネクタ等を接続して利用できます。
- FTDI Basic互換の6ピンコネクタのVDD端子に供給される電圧は、5Vと3.3Vから選択できます。（初期設定は5V）

## 使い方

- （必要であれば同梱の6pソケットをはんだ付けします。）
- [WCH社のドライバのダウンロードサイト](http://www.wch-ic.com/search?q=CH340&t=downloads)から最新のドライバをインストールしておきます。※一部サイトで、古いバージョンのドライバへのリンクが貼られているところがあります。接続後のドライバのインストールに失敗する場合は、最新のドライバをインストールします。
- 市販のUSB Type-Cコネクタを持つケーブルでPCと接続し、ArduinoIDEのシリアルモニタ等のCOMポートを用いるアプリケーションから使用します。

## 使い方（オプション）
- RTS#信号を使用する場合は、基板上のRTS#と示した箇所のランドを使用してください。なおその脇にはGND端子があります。
- 6pコネクタのVDD端子の供給電圧を初期設定の5Vから3.3Vに変更する場合は、裏面ソルダージャンパの「中央-5V間」をカッター等で切断し、「中央-3.3V間」をハンダで接続してください。または切り離した状態で、脇の3p端子にピンヘッダ等を取り付けて3.3V/5Vを切り替えられるようにしてください。
- USB Type-Cコネクタ脇の2組の2p端子は無接続です。ブレッドボード等に固定するヘッダピンを取り付けるなどに使用できます。

## （自作する方向け）作り方

- 基板データ(KiCAD)またはそこから生成したガーバーデータを使って、基板を製造します。
- 部品を入手します。
-- [CH340K](https://akizukidenshi.com/catalog/g/gI-16306/]
-- [USB Type-Cコネクタ](https://akizukidenshi.com/catalog/g/gC-14356/)
-- 0.1uFチップコンデンサ(1608サイズ)：：2個
-- 1kΩチップ抵抗(1608サイズ)
-- 5.1kΩチップ抵抗(1608サイズ)：2個
-- 緑チップLED(1608サイズ)
-- [350mAポリスイッチ(3216サイズ)])https://akizukidenshi.com/catalog/g/gP-13490/)
-- [ピンソケット6p](https://akizukidenshi.com/catalog/g/gC-03784/)
- 基板上に部品をとりつけます。

## Author

Junichi Akita (akita@ifdl.jp, @akita11)

