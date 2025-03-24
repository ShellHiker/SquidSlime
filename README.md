# 概要
SlimeVRの6センサー接続版になります．<br>
ある程度電子工作に慣れていない自分でも組み立てができるように，そして安価にできることを心掛けています．<br>
部品はすべてネット注文できるかと思います．<br>
材料費はおおよそ1万円となりますが，搭載するセンサーによっては値段が変化するので気を付けてください．

## はじめに
はんだ付けを行う際はやけどに十分注意してよく換気をしながら行ってください．<br>
以降に書きますが充電回路周りに関する注意点は必ず読んでください．<br>
Autodesk fusionの非商用ライセンスを使って製作しているのでSTLファイルの商用利用は禁止します．<br>

## 充電回路周りに関して
火災等につながる恐れがあるので十分注意して組み立てに臨んでください．
* 注意点1 : 18650充電池に関して
  > TP4056充電モジュールに加工を加えない場合は18650電池は保護回路のあるものか，充電電流が1Aに耐えるものを使ってください．<br>
  > また，電池ボックスに18650電池をはめたままはんだ付けを行わないでください．
* 注意点2 : TP4056充電モジュールに関して
  > 上記の通りに18650電池を変えない場合，充電電流を調整しているチップ抵抗を交換してください．[参考サイト](https://labo.mycabin.net/electronics-programming/1304/)<br>
  > 交換する場合は充電口がmicro USBのものがやりやすいようです．<br>
  > また，モバイルバッテリーで運用する場合は充電ポートから給電しながら使用せずにESP側のUSBポートから給電を行い，18650電池を取り外してください．<br>
  > 18650充電池に充電しながらの使用はしないでください．

## ファームウェアに関して
ファームウェアを書き込む際はファームウェアフォルダのみをVisual studio codeに読み込ませて下さい．<br>
取り付けたセンサーに合わせて/src/defines.hを書き換えてください．（初期状態はLSM6DSVに設定しています）<br>
29,30行目のセンサーの種類，32,33行目の取付角度を適宜調節してください．<br>
platformio.iniを書き換えるとseeed studio esp32c6も使えると思いますがチップアンテナの強度がそれほど強くないのでアリエク等でアンテナを追加購入しない場合お勧めしません．<br>

## 部品購入リスト
AliExpressで購入する際は海外サイトですので普段より一層注意してPayPalを使うなど行ってください．
<table>
  <tr>
    <th>部品名</th>
    <th>購入先</th>
    <th>備考</th>
  </tr>

  <tr>
    <td>TP4056充電モジュール</td>
    <td><a href="https://amzn.asia/d/jdhtNvE" target="_blank">Amazon</a></td>
    <td>Type-C接続のもの．<br>Aliexpressでは山の数ほどあるので自身で選んでください．</td>
  </tr>
  <tr>
    <td>滑り止め付き身体固定ベルト</td>
    <td><a href="https://amzn.asia/d/c1qFxLP" target="_blank">Amazon</a></td>
    <td></td>
  </tr>
  <tr>
    <td>18650電池ボックス</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g129374/" target="_blank">秋月電子</a></td>
    <td>表面実装のもの</td>
  </tr>
  <tr>
    <td>seeed studio ESP32S3</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g118078/" target="_blank">秋月電子</a><br>
    <a href="https://ssci.to/8968" target="_blank">スイッチサイエンス</a><br>
    <a href="https://ja.aliexpress.com/item/1005004788285643.html" target="_blank">AliExpres</a></td>
    <td>AliExpressで購入する場合は技適マークを確認</td>
  </tr>
  <tr>
    <td>金属皮膜抵抗 1/2W 100kΩ</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g116656/" target="_blank">秋月電子(199個入り)</a><br>
    <a href="https://amzn.asia/d/145EU7i" target="_blank">Amazon(100個入り)</a><br>
    <a href="https://amzn.asia/d/buKsb9Y" target="_blank">Amazon(1個から)</a><br>
    <a href="https://ja.aliexpress.com/item/1005005466858774.html" target="_blank">AliExpress</a></td>
    <td></td>
  </tr>
  <tr>
    <td>金属皮膜抵抗 1/2W 30kΩ</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g116650/" target="_blank">秋月電子(100個入り)</a><br>
    <a href="https://amzn.asia/d/28bEFrl" target="_blank">Amazon(1個から)</a><br>
    <a href="https://ja.aliexpress.com/item/1005005466858774.html" target="_blank">AliExpress</a></td>
    <td></td>
  </tr>
  <tr>
    <td>整流ダイオード 1N5819</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g117244/" target="_blank">秋月電子</a><br>
    <a href="https://amzn.asia/d/dgEWyhH" target="_blank">Amazon(100個入り)</a><br>
    <a href="https://amzn.asia/d/deLb5V1" target="_blank">Amazon(1個から)</a><br>
    <a href="https://ja.aliexpress.com/item/1005001552094086.html" target="_blank">AliExpress(50個入り)</a></td>
    <td></td>
  </tr>
  <tr>
    <td>2回路3接点スイッチ(SK-12D11)</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g115703/" target="_blank">秋月電子</a>
    <a href="https://ja.aliexpress.com/item/1005007876765927.html" target="_blank">AliExpress</a></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td>本体接続用ケーブル細いもの:<a href="https://akizukidenshi.com/catalog/g/g111091/" target="_blank">秋月電子</a><br>
        もしくは<br>
        本体接続用ケーブル太いもの:<a href="https://akizukidenshi.com/catalog/g/g111611/" target="_blank">秋月電子</a></td>
    <td></td>
  </tr>
  <tr>
    <td>18650充電池</td>
    <td><a href="https://item.rakuten.co.jp/3rwebshop/3r-ev18650/" target="_blank">楽天</a></td>
    <td>保護回路付きのもの</td>
  </tr>
  <tr>
    <td>ケース用ねじM2L16-4本　M2L8-20本</td>
    <td><a href="https://amzn.asia/d/12LWxDU" target="_blank">Amazon</a></td>
    <td>L16の方をメイン基板ケースに，L8の方を拡張センサ基板ケースに使用してください</td>
  </tr>
  <tr>
    <td>JST PH 4pin(ハウジング)</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g112797/" target="_blank">秋月電子</a>
    <a href="https://amzn.asia/d/9pRjg2p" target="_blank">Amazon</a><br>
    <a href="https://ja.aliexpress.com/item/1005003164558805.html" target="_blank">AliExpress</a></td>
    <td>PAコネクタのほうが強度が強いが国内で手に入りにくいので割愛<br>PHコネクタ関連3点は無くても接続には問題ないので使うかどうかは任意</td>
  </tr>
  <tr>
    <td>JST PH 4pin L字(コネクタ)</td>
    <td><a href="https://item.rakuten.co.jp/mutsuura/10549889/" target="_blank">楽天</a><br>
    <a href="https://amzn.asia/d/9xwTnSv" target="_blank">Amazon</a><br>
    <a href="https://ja.aliexpress.com/item/33053313994.html" target="_blank">AliExpress(L字)</a></td>
    <td>サイド型は秋月では手に入らないので注意</td>
  </tr>
  <tr>
    <td>JST PH 4pin(圧着端子)</td>
    <td><a href="https://akizukidenshi.com/catalog/g/g112809/" target="_blank">秋月電子</a><br>
    <a href="https://amzn.asia/d/2E6wWLw" target="_blank">Amazon</a><br>
    <a href="https://ja.aliexpress.com/item/1005007388697939.html" target="_blank">AliExpres</a></td>
    <td>落ちた時に見つけづらく，踏んだ時めちゃくちゃ痛いのでLEGOより凶悪</td>
  </tr>
</table>

## センサーリスト
<table>
  <tr>
    <th>センサー種類</th>
    <th>購入先</th>
    <th>備考</th>
  </tr>
  <tr>
    <td>LSM6DSV</td>
    <td><a href="https://shironekya.booth.pm/items/5606882" target="_blank">booth(白猫屋さん)</a></td>
    <td></td>
  </tr>
  <tr>
    <td>LSM6DSO</td>
    <td><a href="https://shironekya.booth.pm/items/6048000" target="_blank">booth(白猫屋さん)</a></td>
    <td></td>
  </tr>
  <tr>
    <td>LSM6DSR</td>
    <td><a href="https://shironekya.booth.pm/items/6098975" target="_blank">booth(白猫屋さん)</a></td>
    <td></td>
  </tr>
  <tr>
    <td>ICM24688</td>
    <td><a href="https://shironekya.booth.pm/items/6053051" target="_blank">booth(白猫屋さん)</a></td>
    <td></td>
  </tr>
  <tr>
    <td>BMI270</td>
    <td><a href="https://shironekya.booth.pm/items/5605683" target="_blank">booth(白猫屋さん)</a></td>
    <td></td>
  </tr>
</table>

## JLCPCBでの電子基板発注方法
いずれも基板の厚みを1.0mmで発注してください．<br>
* ガーバーファイルを使って発注する方法（おすすめ）<br>
  > /PCB/GeneralGerber/のZipファイルを解凍せずにJLCPCBでアップロードしてください<br>
* EasyEDA 経由で発注する方法<br>
  > あらかじめJLCPCBに登録，ログインしておいてから/PCB/EasyEDAのフォルダをEasyEDAで読み込んでFabricationからOne-click Order PCB/SMTを選択，＞No continue order＞Yesで発注してください．

## ケースについて
今回はSTLファイルを同梱していますが，固定等がしっかりできるのであれば自作したり，100均等で売られているものを流用しても構いません．<br>
ベルトを通す幅によってbottom部分を分けています．<br>
JLC3DPに発注する際の印刷方式はSLSを推奨します．<br>
また，きれいな作り方ではないですがfusionのファイルも同梱しているので加工等はお好きにどうぞ．<br>

## 工具・消耗品
[PHコネクタ圧着工具](https://amzn.asia/d/fIVv21o)<br>
[ワイヤーストリッパー](https://akizukidenshi.com/catalog/g/g129524/)<br>
[はんだごて](https://amzn.asia/d/cYUjaue)<br>
[鉛フリーはんだ](https://akizukidenshi.com/catalog/g/g129524/)<br>