# 実践編

まず、アプリケーションを起動しましょう。[ダウンロードしてから初回の起動時はシステムに起動をブロックされることがありますが、無視して起動してください。](../Troubleshooting/index.md#_2)

![Maxアプリケーションのスクリーンショット。]()

音声用プログラムのフォルダ内の、`ccbt_tonechime_sensor`というMaxプロジェクトファイルをダブルクリックすると、Max上で音声解析と照明制御用のアプリケーションが起動します。

![映像アプリケーションのスクリーンショット。]()

映像アプリケーションフォルダ内の `Tonechime_VideoSystem` というアプリケーションをダブルクリックすると、映像アプリケーションが起動します。この時、外部ディスプレイを繋いでいると、映像アプリケーションが自動的に全画面で表示されます。メインディスプレイには、小さな操作ウィンドウが表示されます。アプリケーションを立ち上げたら、はじめに、オーディオインターフェースやDMXの接続設定をします。

![オーディオ設定のウィンドウ。]()

まず、右上の、"Open Audio Setting"ボタンをクリックします。新しくウィンドウが立ち上がるので、うえから2番目のDRIVERという項目で”ad_portaudio”または"Windows DirectSound"（Macなら”Core Audio”）、3番目のINPUT DEVICEで、使用しているオーディオインターフェースの名前を選択します。選択したらオーディオ設定ウィンドウを閉じます。

”DSP”のボタンが灰色なら、クリックして緑色になるようにします。

![DMX設定部分を囲んだスクリーンショット]()

その下のDMXのボタンも緑色になるようにクリックします。USB DMX PROが接続されていれば、右隣のアイコンが緑色に光り、"Connected"と表示されます。

> [!NOTE]
> アプリケーションは、USB経由で接続されているシリアル通信を行う機器を自動的に検出します。複数台シリアルデバイスが接続されているとUSB DMX PRO以外の機器に接続を試みてしまうので、システムに関係ないUSB機器は接続しないようにしてください。

![OSC設定部分を囲んだスクリーンショット]()

さらにその下の、"OSC"ボタンも緑色になるように、また"LOCAL_MODE"も黄色になるようにクリックします。

> [!NOTE]
> "LOCAL_MODE" をオフにすると、別のコンピューターで起動している映像アプリケーションと同期することができます。映像アプリケーションを立ち上げているコンピューターのIPアドレスをportの左隣のaddressという欄に入力してください。

![設定保存部分を囲んだスクリーンショット]()

右上の”Save Config”ボタンを押してください。接続している機器の構成が同じなら、次回アプリケーションを立ち上げた時に、オーディオインターフェースの設定を含め、現在のパラメーターが自動で復元されます。

> [!NOTE]
> パラメーターは`data/main.json`というファイルの中に書き込まれています。JSONデータ内の`pattrstorage/slots/1/data` を直接編集することもできます。

## トーンチャイムの音程と音量の設定

![音程設定部分を囲んだスクリーンショット]()

音声解析プログラムでは、あらかじめ使うトーンチャイムの音程をプログラム側で指定することで、余計なノイズの検出を防いでいます。音声解析アプリの画面下側で、トーンチャイムの音程と音量をそれぞれ調節することができます。

”Pitch”というダイアルをドラッグして、使っているトーンチャイムの音程の名前に合わせます。また、右側のBPFというボタンが黄色く光っていることを確認してください。

> [!NOTE]
> ソフトウェア上では黒鍵の音程が`A#4`や`D#4`などシャープで表記されてますが、トーンチャイムでは`B♭4`や`E♭4` などフラット表記になっているので、間違えないようにしましょう。

次に、コンタクトマイクの音量（感度）を設定しましょう。トーンチャイムを叩いた時に、gainと書いてある部分のメーターに音の大きさが表示されます。

![入力つまみ部分の写真]()

オーディオインターフェースの入力ゲインのつまみを、強めにトーンチャイムを叩いた時に、メーターが赤や黄色にならない程度まで右に回して上げていきます。

もし、オーディオインターフェース側でピーク過大入力のランプが点灯したり、つまみを上げ切ったけどまだ音量が小さい、という場合には、アプリケーション上でゲインのメーターをドラッグし、さらに音量を調整してください。

複数トーンチャイムを使う時は、すべてのチャンネルでピッチと音量の調整を行なってください。再び、"Save Config"を押して、設定を保存しておきましょう。

## 照明・映像の設定

![ライト周りのスクリーンショット]()

照明の設定を行います。まず、LightUSB DMX PRO Brightnessというスライダーを左右にドラッグして、ライトの明るさが変化するかチェックしましょう。これを動かしても明るさが変化しない場合は、[セットアップ編でのDMXや照明の接続、ディマーの設定に問題があります](../Troubleshooting/index.md#_7)。

トーンチャイムを強めに叩いた時に、Light Brightnessが右端までいかなければ、上の方にある、Range-Inputというスライダーを、少しずつ下げてみます。

映像システムでは、チャンネルごとに設定された色を持つ円が、音量に応じて、大きさを変化させます。

この時、音量によって3段階で映像効果が変化します。大・中・小をどの程度の音量で分割するかは、Detection ThresholdのHigh,Mid,Lowというスライダーで設定します。

アプリ下側のVideoという場所で、実際の音量の変化と、3段階の分割位置が表示されているので、音量を変えながら叩いてみて、ちょうど良い分割地点を探してみてください。

映像アプリケーションの方では、チャンネルごとの色を設定することができます。

実際には音が鳴っていないのに、ライトが細かくちらつく場合は、Smoothingというスライダーの値を上げてください。

同じように、映像の方にも細かく反応がある場合は、Detection Thresholdのattackというスライダーを上げてみてください。

![スムージング関係のスクリーンショット]()

アプリケーションを終了する前に、うまく動いている状態で再度Save Configを押しておきましょう。

右上（macOSでは左上）の❌ボタンで音声アプリケーションは終了できます。映像アプリケーションの設定は自動的にセーブされます。画面右下の終了ボタンをクリックして終了します。

> [!WARNING]
> 映像アプリケーションの終了は、右下の終了ボタンで終了しないと情報が保存されません。ウィンドウ上の❌ボタンで終了しないようにしてください。