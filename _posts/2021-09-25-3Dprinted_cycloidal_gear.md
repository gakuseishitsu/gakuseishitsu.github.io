---

layout: post

title: 3Dプリンタでサイクロイド減速機 その1

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg1.png">

# はじめに
[前回ミニッツリピータの打鍵機構の試作機を作ったとき](https://gakuseishitsu.github.io/strike_mechanism/)、駆動源は単純な錘式にした.  
つくるのは楽だったけど錘が重たいから取り回しも面倒だし, ラチェット機構すら入れてなかったから巻き戻すのも面倒だし, 機構の下にスペース取らないといけないから置き場所も限られるしで作った後が大変だった.  
そこで今回もっと良い駆動源を作ることにした.  
普通の巻きばね+ラチェット機構でも良かったけど, 最近モーター回してなかったので電動式にすることにした.  

# MJBOT moteus
好奇心からモータとしてあまりいじったことがなかったBLDCモータを使ってみることにした.  
世の中で売られている(有名な?)BLDCモータ+ドライバとしてODriveやらMIT Mini CheetahやらBGC3.1やらB-G431B-ESC1やらいっぱいあったけど, サイズ感やモータ、ドライバ、エンコーダが一体になっていて楽という点から[MJBOT moteusのキット](https://mjbots.com/collections/servos-and-controllers/products/moteus-r4-8-developer-kit)を使うことにした.  

設計に使うため早速モデリングした.  
モータのSTLが公開されていたのでそこは楽だった. (基板回りは大変だった)  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg2.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg3.png">

# 減速機の設計
結構強いトルクも出せそうなのでそのままつなごうかとも思ったが、超低速で回してみたらさすがにカクカクしていたので適当な減速機をかませることにした.  
[昔ハーモニックドライブを作ったことがあった](https://gakuseishitsu.github.io/3Dprinted_harmonic_drive/)ので今回はサイクロイド減速機に挑戦してみることにした.  
[トロコイド曲線を書くFusion360のスクリプトを公開されている方](https://woodencaliper.hatenablog.com/entry/2018/12/24/173522)がいたので活用させていただいた.  
周辺も含めて早速設計した.  
手元にちょうどいいベアリングが一個だけあったので入力軸の部分に使った.  
他の回転指示部は摺動でがんばってもらった.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg7.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg4.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg5.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg6.png">

# 製造
適当なクリアランス調整して早速印刷して組み立てた.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg8.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg9.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg10.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210925_cycloidal_gear1/cg11.jpg">

動作も無事確認できた.  
バックドライブもちゃんとできた.  

<iframe width="560" height="315" src="https://www.youtube.com/embed/BEuPRBtjKtU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">サイクロイド減速機動いた. 出力軸にもベアリング欲しい. <a href="https://t.co/BlY9sETAeW">pic.twitter.com/BlY9sETAeW</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1441601730177757190?ref_src=twsrc%5Etfw">September 25, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# おわりに
動いたは良いが, 出力軸も一緒に偏心してるしシャリシャリ言うしやっぱり出力軸にもベアリング入れたほうがいいと思った.  
そして香箱として使うにはでかすぎた.  
試作機2号早速設計開始.  

以上  