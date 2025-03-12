# 概要
SlimeVRの6センサー運用版になります．
ある程度電子工作に慣れていない自分でも組み立てができるように，そして全てネット注文できる部品で作ることを心掛けました．
搭載するセンサーによっては値段が変化するので気を付けてください．

## はじめに
* はんだ付けを行う際はやけどに十分注意してよく換気をしながら行ってください．
* 以降に書きますが充電回路周りに関する注意点は必ず読んでください．
* STLファイルはfusion360の非商用ライセンスを使って製作しているので商用利用は禁止します．

## 充電回路周りに関して
火災等につながる恐れがあるので十分注意して組み立てに臨んでください．
* 注意点1 : 18650充電池に関して
  > TP4056充電モジュールに加工を加えない場合は18650電池は保護回路のあるものか，充電電流が1Aに耐えるものを使ってください．
  > また，電池ボックスに18650電池をはめたままはんだ付けを行わないでください．
* 注意点2 : TP4056充電モジュールに関して
  > 上記の通りに18650電池を変えない場合，充電電流を調整しているチップ抵抗を交換してください．[参考サイト](https://labo.mycabin.net/electronics-programming/1304/)
  > 交換する場合はmicro USBのものがやりやすいようです．
  > また，モバイルバッテリーで運用する場合は充電ポートから給電しながら使用せずに通信ポートから給電を行い，18650電池を取り外してください．
  > 18650充電池に充電しながらの使用はしないでください．

## 部品購入リスト
* 国内サイト / Amazon Japan
  * Amazon
  > * [TP4056充電モジュール](https://amzn.asia/d/jdhtNvE)
  > * [JST PHコネクタ](https://www.amazon.co.jp/dp/B08JYNRTS1?ref=ppx_yo2ov_dt_b_fed_asin_title)
  > * [ケース用ねじm2l8-4本 m2l6-20本](https://amzn.asia/d/12LWxDU)
  > * [滑り止め付き身体固定ベルト](https://amzn.asia/d/c1qFxLP)

  * 秋月電子
  > * [18650電池ボックス](https://akizukidenshi.com/catalog/g/g129374/)
  > * [seeed studio ESP32S3](https://akizukidenshi.com/catalog/g/g118078/)
  > * [金属皮膜抵抗 1/2W 100kΩ](https://akizukidenshi.com/catalog/g/g116656/)
  > * [金属皮膜抵抗 1/2W 30kΩ](https://akizukidenshi.com/catalog/g/g116650/)
  > * [整流ダイオード 1N5819](https://akizukidenshi.com/catalog/g/g117244/)
  > * [2回路3接点スイッチ](https://akizukidenshi.com/catalog/g/g115703/)
  > * [センサー延長用ケーブル(細いもの)](https://akizukidenshi.com/catalog/g/g111091/)
  > * もしくは
  > * [センサー接続用ケーブル(太いもの)](https://akizukidenshi.com/catalog/g/g111611/)

  * 楽天
  > * [保護回路付き18650電池](https://item.rakuten.co.jp/3rwebshop/3r-ev18650/)

  * booth　（いずれかのセンサーを選択）
  > * [LSM6DSV](https://booth.pm/ja/items/5606882)
  > * [LSM6DSO](https://booth.pm/ja/items/6048000)
  > * [LSM6DSR](https://booth.pm/ja/items/6098975)
  > * [ICM24688](https://booth.pm/ja/items/6053051)

## JLCPCBでの電子基板発注方法
* いずれも基板の厚みを1.ommで発注してください．
* ガーバーファイル経由で発注する方法（おすすめ）
  > /PCB/GeneralGerber/のZipファイルを解凍せずにJLCPCBでアップロードしてください
* EasyEDA 経由で発注する方法
  > あらかじめJLCPCBに登録，ログインしておいてから/PCB/EasyEDAのフォルダをEasyEDAで読み込んでFabricationからOne-click Order PCB/SMTを選択，＞No continue order＞Yesで発注してください．

## ケースについて
* 今回はSTLファイルを同梱していますが，固定等がしっかりできるのであれば自作したり，100均等で売られているものを流用しても構いません．
ベルトを通す幅によってbottomを分けています．
また，fusionのファイルも同梱しているので加工等はお好きにどうぞ．

## 工具・消耗品
> * [PHコネクタ圧着工具](https://amzn.asia/d/fIVv21o)
> * [ワイヤーストリッパー](https://akizukidenshi.com/catalog/g/g129524/)
> * [はんだごて](https://amzn.asia/d/cYUjaue)
> * [鉛フリーはんだ](https://akizukidenshi.com/catalog/g/g129524/)