# scrcpy

> androidの画面を僕のPCとUSBケーブルとなんらかのソフトのみを使ってミラーできる？

できるよ。Androidなら、**USBケーブルだけ＋PC側のソフト**でかなり快適にミラーリングできる。

Linuxなら一番おすすめは **scrcpy**。

* USB接続
* Android側で「USBデバッグ」を有効化
* PCで `scrcpy` を実行
* Androidの画面がPCのウィンドウに表示される
* マウス・キーボード操作もできる
* 基本的にAndroid側へ専用アプリをインストールする必要なし
* Wi-Fi不要でUSBだけでも動く

Arch Linuxなら、

```fish
sudo pacman -S scrcpy
```

で入れられる。

その後、

```fish
scrcpy
```

だけでOK。

ちなみに、**画面をPCに映すだけならかなり軽い**し、USB接続なら遅延も小さい。
「Android → PCへの画面ミラー＋PCからAndroid操作」という用途なら、まずscrcpyを試すのがいいと思う。

> USBデバックはなに？file transfer, usb tethering, midi, ptpしかないけど

それはスマホの**USB接続モード**だね。
「USBデバッグ」はそこにはなくて、**Androidの開発者向けオプション**にある。

だいたいこうする：

1. **設定 → デバイス情報**（または「端末情報」）を開く
2. **「ビルド番号」**を探す
3. 「ビルド番号」を**7回くらいタップ**
4. 「開発者向けオプションが有効になりました」みたいな表示が出る
5. 設定に戻って **「開発者向けオプション」**を開く
6. **「USBデバッグ」**をONにする
7. USBでPCにつなぐ
8. スマホに「このパソコンをUSBデバッグで許可しますか？」と出たら**許可**

そのあとPCで

```fish
scrcpy
```

で映せるはず。

ちなみに、今出ている

* File transfer
* USB tethering
* MIDI
* PTP

は**USBデバッグとは別物**。
scrcpyでは、基本的に「File transfer」を選んでおけば大丈夫。
