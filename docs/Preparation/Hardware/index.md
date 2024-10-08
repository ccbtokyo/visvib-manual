# 準備-ハードウェア編

![トーンチャイムにセンサーを取り付けた完成状態の画像。](../../img/tonechime-complete.jpg)

VisVibのシステムでは、トーンチャイムに取り付けた振動センサー（コンタクトマイク）をコンピューター上で解析して、照明や映像に変換します。

## 構成別必要機材

オリジナルの構成は、トーンチャイム8台を使い、無線信号でコンピューターへ情報を送っています。ただし、この構成は大掛かりかつ高価になるため、本ドキュメントでは以下の3パターンの構成例を示します。

- トーンチャイムx8 無線接続
- トーンチャイムx2 無線接続
- トーンチャイムx2 有線接続

|  カテゴリ   |                     | 8台-無線| 2台-無線| 2台-有線 | 
| :------: |---------------------| :----: | :----: | :----: | 
| 楽器　    | トーンチャイム             |8       |2       |2      | 
| PC       | コンピューター             |1       |1       |1      |
| 音関係    | コンタクトマイク（自作）　　　 　   |8       |2       |2      | 
| 　　　    | オーディオトランスミッタ        |4       |1       |-      | 
|          | 3.5mmプラグ-6.3mmプラグ変換 |-      |-       |2      |
| 　　　    | オーディオインターフェース       |[A](#a)|[B](#b) | [B](#b)|
| 照明　　　| ディマー                |2      |1       |2      |
| 　　　　　 | ENTEC DMX USB PRO   |1      |1       |1      |
| 　　　　　 | XLRケーブル             |2      |2       |2       |
| 　　　　　 | XLRF3-M5ピン変換        |1      |1       |1       |
| 　　　　　 | 白熱電球              　 |8      |2       |2       |
| 映像　    | ディスプレイorプロジェクター     |1       |1       |1      |
|  　　　   | 映像接続ケーブル（HDMI等）　 　  |1       |1       |1      |

照明と映像機材については、どちらか片方だけの使用でも問題ありません。

## 楽器

[SUZUKI トーンチャイム](https://www.suzuki-music.co.jp/products/36403/)

棒状のハンドベルのような楽器です。ワークショップでは、中音域の基本セットHB-250Nの中から8音を選んで使用しています。マイクを取り付けるための3Dプリント製アタッチメントはこの基本セットの楽器の太さ2種類に対応しています。



## PC関係、映像関係

本ドキュメントで使用するコンピューターはWindows環境を想定していますが、macOS環境でも動作できます。

メモリ：8GB
OS：Windows 10以上/macOS 13(Ventura)以上

映像システムを使う場合は、コンピューターは外部ディスプレイ接続ができる必要があります。

## 音関係

### コンタクトマイク

![特製マイクロフォンの画像。左側にはカバーありバージョン、右側にはカバーなしのバージョンが置かれている。](../../img/microphone.JPG)

コンタクトマイクは特製のものを使用します。このマイクは、空気振動ではなく、貼り付けた物体の振動を直接拾うものです。

このマイクは、ピエゾ素子という、安価な部品をケーブルにはんだ付けすることで、簡単に作ることができます。

マイクの作成方法は、**[特製コンタクトマイクロフォン（振動センサー）の制作手順](make-contact-microphone.md)** というドキュメントを参照してください。

### オーディオインターフェース

マイクから取り込んだ音をコンピュータに取り込むためのデバイスです。

#### A

[MOTU UltraLite Mk5](https://www.soundhouse.co.jp/products/detail/item/291119/)

RME FireFace UFXなど、ライン入力が8ch以上使用できるインターフェースであれば他機種でも運用可能です。

#### B

[Roland Rubix24](https://www.roland.com/jp/products/rubix24/)

Aを所持している場合はそのまま使用しても問題ありません。

### オーディオトランスミッタ（無線接続の場合）

[SENNHEISER EW 122P G4-JB（もしくはEW112P）](https://www.soundhouse.co.jp/products/detail/item/254766/)

トーンチャイムからオーディオインターフェースまでの接続を無線で行う場合、トランスミッタを使用します。

このトランスミッタは最大で8台まで同時使用が可能であること、B帯を用いたアナログ伝送で遅延が少ないことを理由に採用しています。（会場で他のB帯を使用する機器と無線のチャンネルが干渉しないか注意してください。）

より少ないチャンネル数の構成の場合、もっと安価なものでも問題ありません。2.4GHz帯などを使用するデジタルのトランスミッタや、Bluetoothのトランスミッタでも問題ありませんが、遅延が発生する場合があります。

## 照明

### ディマー

![ディマーのアップ画像。](../../img/dimmerpack.jpg)

[AMERICAN DJ / DP415R](https://www.soundhouse.co.jp/products/detail/item/252223/)

- DMX信号を使ってAC100Vコンセントの電圧を制御する機器です。
- 他の代替候補としては、Elation Cyber PakやLITE-PUTER DX-402Aなどがあります。
- どれも1台で4チャンネルまで制御できるため、5台以上照明を使う場合は2台必要です。

### ENTEC DMX USB PRO

![DMX USB PROのアップ画像](../../img/dmxusbpro.jpg)

[ENTEC DMX USB PRO](https://www.enttec.com/product/dmx-usb-interfaces/dmx-usb-pro-professional-1u-usb-to-dmx512-converter/)

- コンピューターからUSB経由でDMX信号を制御するための変換アダプタです。

加えて以下のケーブルと変換アダプタも用意します。

- XLRケーブル 3ピンのオーディオ用と同じものでOKです。長さは必要に応じて。
- XLRメス3ピン-XLR5オスピン　変換アダプタ
  - [NEUTRIK NA3F5M](https://www.soundhouse.co.jp/products/detail/item/236711/)など。

### 白熱電球

クリップライトなど、普通のコンセントに挿さる白熱電球ならなんでも問題ありません。ただし、蛍光灯、LED球は原則使用できません。調光対応のものであれば使用できるが、一定以上の暗さになると完全消灯してしまうため推奨しません。

## 映像

プロジェクターもしくはディスプレイを1台使用します。機種や解像度には特別な制限はありません。

コンピューターと接続するためのケーブル（HDMIやDisplayPortなど）や変換アダプタは機種に合わせて用意してください。
