---

layout: post

title: 3Dプリントしたハーモニックドライブ

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200710_3Dprinted_harmonic_drive/HD_1.jpg">

# はじめに
[新しい3Dプリンタを手に入れて](https://gakuseishitsu.github.io/QIDI_Xplus/)性能を試すいいネタが無いかと考えた。
いままで工作で歯車が必要な時はCNCフライスでやっていたが3Dプリンタでも使える歯車作れないかなと思って歯車を使った何か無いか調べ始めた。
そこで目に留まったのがハーモニックドライブ。歯車に加えて構造の弾性変形を利用するのでちょうどいいターゲットだと思って設計を開始した。

# 試作1回目
原理を調べて見様見真似でまずはモデリングしてみた↓。回転源は分解した前の3Dプリンタのエクストルーダについていたよくあるステッピングモータ。

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200710_3Dprinted_harmonic_drive/HD_8.png">

ギアのモジュールは攻めて0.5にしてみた。また出力軸側から見てウェーブジェネレータとフレクスプラインの動きがよくわかるように肉抜きだらけにしている。

印刷してみたら、残念ながら歯車がつぶれていてうまくかみ合わなかった。さすがに0.4mmノズルのPLAでモジュール0.5は厳しかった。他についても肉抜きしすぎて簡単にポキポキ折れてしまった。気を取り直して2回目開始

# 試作2回目
1回目の失敗を生かして今回はモジュール2にした、また構造の厚みを全体的に増やした↓。
今回は印刷はうまくできた。

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200710_3Dprinted_harmonic_drive/HD_6.png">

<blockquote class="twitter-tweet"><p lang="zh" dir="ltr">試作一個目. <a href="https://t.co/nXvGk9SRE4">pic.twitter.com/nXvGk9SRE4</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1281207640350011392?ref_src=twsrc%5Etfw">July 9, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

アセンブリしてみて動かしてみたら、変形に耐えられずフレクスプラインが割れてしまった(以下動画)。そもそもPLA使っているのが間違いだがもっと変位に耐えられる形にしないといけない。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">いままで名前はしってたけど原理は知らなかったやつ. 壊れながら動いてるw. <a href="https://t.co/M5Isnx5FcH">pic.twitter.com/M5Isnx5FcH</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1281207381771161601?ref_src=twsrc%5Etfw">July 9, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# 試作3回目
フレクスプラインが弾性変形しても割れないように↓のように形状を工夫した。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">フレクスプラインリベンジ <a href="https://t.co/UosTZ4Rtqx">pic.twitter.com/UosTZ4Rtqx</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1281436389754593280?ref_src=twsrc%5Etfw">July 10, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200710_3Dprinted_harmonic_drive/HD_7.png">

今度はちゃんと変形に耐えて動作してくれた、完成。

<blockquote class="twitter-tweet"><p lang="und" dir="ltr"><a href="https://t.co/xFU8xwXpdg">pic.twitter.com/xFU8xwXpdg</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1281501572430618624?ref_src=twsrc%5Etfw">July 10, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Nwc8ObIFlbs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200710_3Dprinted_harmonic_drive/HD_1.jpg">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200710_3Dprinted_harmonic_drive/HD_2.jpg">

# おわりに
ちゃんとしたものを作るならABSとか変形に強いものにしたほうがいい。
手のりサイズでコンパクトかつ好みの見た目にできて満足である。

以上


# 参考文献
[1] [ハーモニックドライブ®の原理](https://www.hds.co.jp/products/hd_theory/)

[2] [東京ロボティクス開発者ブログ メカの話-減速機①](https://blog.robotics.tokyo/archives/321)