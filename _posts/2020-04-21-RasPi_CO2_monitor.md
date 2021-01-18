---

layout: post

title: CO2モニタ

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200421_RasPi_CO2_monitor/CO2_thumbnail.jpg">

# はじめに

自分もテレワークになり[いい椅子](https://twitter.com/YASUBE_T_AU/status/1247811023697883136 "アーロンチェア")を買ったりとWFH環境を整えつつある。  
オフィスではエアコンや換気、照明などで作業をするのに適した環境にコントロールされているが家では普段室温程度しか気にしていない。  
窓を閉め切っていたりすると室内のCO2濃度が上がり眠くなったり集中が途切安くなったりするらしい。ずっと窓を開けて開放していくわけにもいかないため適度な間隔で換気できるようにCO2モニタを用意しようと考えた。
市販品を購入しても良かったがSNSでCO2モニタを作ったという事例をちらほら見かけたので自分も作ろうと思った。

ちなみに環境のCO2濃度と人体への影響は↓みたいになっているらしい([出典](https://www.asteria.com/jp/warp/blog/20180314/30301.html))。1000ppmを超えたら換気するような感じにしたい。

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200421_RasPi_CO2_monitor/CO2_3.png">


# CO2センサ(MH-Z19B)
趣味の電子工作レベルで扱えそうなCO2センサを調べていたら[MH-Z19B](https://www.amazon.co.jp/s?k=MH-Z19B&i=electronics&__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&ref=nb_sb_noss_2)というものが見つかった。  
シリアル通信で扱えてかつネットにいっぱいサンプルが転がっていたので購入した。  
届いてすぐRasPi zero wにつないで動かしてみた↓。 最初繋いだ時は2000ppm以上の値がでてて心配したが、外においてしばらくしたらちゃんと400ppm程度に落ち着いていた。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">CO2センサが届いたから弄ってる <a href="https://t.co/izl9Y8BS0E">pic.twitter.com/izl9Y8BS0E</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1249676548514254849?ref_src=twsrc%5Etfw">April 13, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# フック作り
RasPiは別でも使うだろうし、しっかりした筐体を作るつもりは無かったが、ひっかけて使いたかった(目線くらいの高さで計測したい)のでフックを作ることにした。  
単純にセンサとラズパイを締結できてひっかける部分があるものでよかったが、思いつかないような面白い形状が出てこないかと期待してAutodesk Fusion360のgenerative design機能を使って形状出力してみた。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">形は面白い. ジェネレーティブデザイン. <a href="https://t.co/SEp9zlTB6c">pic.twitter.com/SEp9zlTB6c</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1252498546151944193?ref_src=twsrc%5Etfw">April 21, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

左上の形が好みだったので(荷重も小さいし評価項目は完全に見た目)それをもとにきれいにモデリングしなおした。

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200421_RasPi_CO2_monitor/CO2_1.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200421_RasPi_CO2_monitor/CO2_2.png">

↓印刷して実際に使っている様子。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">印刷した <a href="https://t.co/V66RT8WWGH">pic.twitter.com/V66RT8WWGH</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1252498739136086016?ref_src=twsrc%5Etfw">April 21, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# おわりに
実際に使っていると換気して窓をしめてからだんだんと値がじわじわ上がっていくのが面白い。
いつもそんなに注視しているわけではないから気づいたら1000ppmを大きく超えているときもあるが実際どれくらい影響が出ているのかはよくわからない。(CO2の値よりも気分展開のために窓を開ける頻度のほうが多い気がする。)

以上


# 参考文献
[1] CO2センサーを利用して部屋のCO2濃度を検出してみた
 - URL:https://www.asteria.com/jp/warp/blog/20180314/30301.html


