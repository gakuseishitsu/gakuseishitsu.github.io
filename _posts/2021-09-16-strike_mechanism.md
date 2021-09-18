---

layout: post

title: ミニッツリピータのための試作1号機

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm22.jpg">

# はじめに
トゥールビヨンの機構を作ってから次はミニッツリピータ作りたいと思ってはいた.  
(うだうだしてたら数年たっていた)  
そんな時, [youtubeで1時間毎のラック/スネイルを用いた打鍵機構を自作されている方](https://www.youtube.com/watch?v=rxM7lk21F0E)を見つけ, モチベーションが急に湧いてきた.    
さらに動画コメントにて機構の参考元の本 ["Clock Repairing as a Hobby"](https://www.amazon.co.jp/Clock-Repairing-Hobby-Illustrated-How/dp/160239153X) が紹介されていたので早速手に入れ読んでみた.  
本には1時間毎と15分毎のラック/スネイルを用いた打刻機構の構造が詳細に説明されていた.  
最終ゴールは1時間毎、15分毎、1分毎の現代の腕時計に組み込まれているようなミニッツリピータ機構であるが, 基本的な部分を知るためまずは真似て早速試作1機目を作ってみようと思った.  

# 主要部品
今回作る試作機はyoutubeにあったものと同じ1時間毎の打鍵機構. まずは主要部品を本の機構の挿絵そのままスキャンしてなぞりながらモデリングした. 本の挿絵はあくまで概念図だったので歯車の比を調整したり, ラックフックとギャザリングパレットの干渉を何とかしたり微妙な調整は必要であった.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm2.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm3.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm4.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm5.png">

# 1回目の設計
主要部品の形と配置が決まったのでフレームやシャフト等の他の部分も検討しまずは1回目の設計を行った.  
機構の動きが見えやすいようにアクリル板の筐体, シャフトは基本Φ2の真鍮丸棒, 主要部品は3Dプリント(PETG), 香箱の駆動源は簡単な錘式, 抑え等は輪ゴムとした.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm6.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm7.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm8.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm9.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm10.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm11.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm12.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm13.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm14.png">

# 設計修正
早速作ろうと材料を買い始めたり部分的な印刷をはじめたが, 案の定問題がいっぱいでてきた↓.  

* アクリル板が思ったより高かったのでフレームも3Dプリント(PETG)に変更
* 3DP歯車&摺動の効率が悪すぎて部分的にベアリング入れたりバックラッシュ大きくしたりしたり変更
* フライ(速度調整用空気抵抗兼回転慣性)が小さすぎてのでサイズ調整
* 打鍵の音が残念過ぎたため自転車ベルに変更
* その他干渉等の設計ミス修正, 組み立てにくさ解消

問題をプチプチつぶしていき最終的な設計に行きついた.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm17.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm18.png">

# 製造過程
作っていて地味に面倒だったのは3Dプリント歯車の層間のblobsの除去.
↓絵のように外周の開始と終点の部分でつなぎ目が盛り上がってしまう(白い部分)  
CURAの設定を詰めれば回避できる気もするが, 面倒だったので今回は突起がでたらカッター等で削り落とした.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm16.png">

↓ フレームを組んだ時の写真. 

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm24.jpg">

3番目の歯車まで入れて初めて回した時, 調整前だったためゴリゴリ.  

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">3つめの歯車まで、3DPの歯車はblobsがつらい。 <a href="https://t.co/6HGOHATtjZ">pic.twitter.com/6HGOHATtjZ</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1435193630159900675?ref_src=twsrc%5Etfw">September 7, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

↓歯車列がだいたい出来上がって回してみたとき. 早いとハンマーが跳ねる.  

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">ぴょんぴょん... <a href="https://t.co/qZdAZdvyXs">pic.twitter.com/qZdAZdvyXs</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1435562470962184201?ref_src=twsrc%5Etfw">September 8, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# 完成
↓もろもろ調整が完了し初めて動いた時.  

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">動いた, 試作機1つめ完成. 続きのquater/minute snailの部分やりたいけどまずは錘式の香箱を変えたい. <a href="https://t.co/KKiTTFPsC0">pic.twitter.com/KKiTTFPsC0</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1438432542584045568?ref_src=twsrc%5Etfw">September 16, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

ちゃんとカメラで動画取ってyoutubeにも上げた

<iframe width="560" height="315" src="https://www.youtube.com/embed/Q2N3c7h2MLw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

後はギャラリー

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm22.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm19.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm20.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210916_strike_mechanism/sm23.jpg">

# おわりに
無事第一歩を踏めた. 進められることはたくさんあるがまずは香箱を錘式から改良することからはじめる予定.    

以上  