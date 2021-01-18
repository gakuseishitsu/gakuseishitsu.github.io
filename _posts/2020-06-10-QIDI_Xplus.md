---

layout: post

title: QIDI X-Plusの購入

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/200610_new_3D_printer/3D.jpg">

# はじめに
3年ほど使っていた3Dプリンタ([UPmini2](https://www.pp3dp.jp/3d004.html))が頻繁に「Nozzle Too Cool」というエラーをはいて止まるようになってしまった。  
きっと接触不良関係だろうと思ってオーバーホールしてみたが症状が改善しなかったのでサポートに出してみたところ基板自体の問題ということが判明し、修理に8万程度かかると言われたので諦めて新しい3Dプリンタを買うことに決めた。  
捨てるのはもったいないから分解して構造を見たり部品取りをしたりして楽しんだ。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">3Dプリンタご臨終で解体。汎用3軸テーブルとして余生を過ごしてもらう。 <a href="https://t.co/68jFbIYe6v">pic.twitter.com/68jFbIYe6v</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1266346843039916034?ref_src=twsrc%5Etfw">May 29, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

# QIDI X-Plus
似たような価格帯(~10万円)で新しい3Dプリンタを探した。
使用人口も多く、定番なのは[Prusa i3 MK3](https://shop.prusa3d.com/en/51-original-prusa-i3-mk3s)だが、リードタイムが長いのとエンクロージャが無いことが気になって他のものも探し始めた。

調べている中で自分がよく見ている[Maker's Museのyoutubeチャンネル](https://www.youtube.com/channel/UCxQbYGpbdrh-b2ND-AfIybg)にQIDI X-Plusのレビュー動画↓を見つけてなかなか良さそうだと思って見ているうちに思い切って決めてしまった。


<iframe width="560" height="315" src="https://www.youtube.com/embed/LhY6hiBaP0k" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


購入に関してどこで買うのが一番良いのがいいのかよく分からなかったので素直に[公式](
sales@qd3dprinter.com)にメールで問い合わせてみたら、ペイパルアカウントに直接料金振り込んでくれたら配送するよ!と帰ってきたので結局amazonもAliexpressも使わず買えた(ディスカウントもしてくれた)。

注文後2日で届いた。中国(浙江省)から発送されたのにそんなに早く届くんだと驚いた。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">新しい3Dプリンタ届いた. QIDI X-Plus. <a href="https://t.co/cHYQRVE2NS">pic.twitter.com/cHYQRVE2NS</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1270666557106950144?ref_src=twsrc%5Etfw">June 10, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

早速付属のPLAでテストプリントしてみた。テスト用Gコードで設定はよくわからないが↓のようにきれいに印刷できていた。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">テスト印刷. 見た目はとてもきれい. <a href="https://t.co/aJ5lPxknch">pic.twitter.com/aJ5lPxknch</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1270705700742688768?ref_src=twsrc%5Etfw">June 10, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 初期不具合
専用スライサ(Qidi Print)でいくつかテストプリントをしていたら↓みたいな問題が発覚した。
XY軸の直角が出ていなくて精度が出ていないようだった。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">X-PLUS, 寸法は厚みを除いてとても良い, XYテーブルの直角はとても悪いということが分かった. <a href="https://t.co/mOBr5FlLH3">pic.twitter.com/mOBr5FlLH3</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1271428389149175809?ref_src=twsrc%5Etfw">June 12, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

サポートに問い合わせてみたら1時間もせず直し方が動画付で送られてきた(すごい!)。
無事傾きが直せて、印刷設定も調整できたので使えるものになってきた。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">XYテーブルの傾きを直したら無事直角がでて完全体になった. <a href="https://t.co/bVmSuukvc7">pic.twitter.com/bVmSuukvc7</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1271623513544130561?ref_src=twsrc%5Etfw">June 13, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


## いろいろ印刷してみた
昔使ってたプリンタのスライサではインフィルの設定の自由度がそんなになかったのでQIDI printやCURAでいろいろな設定ができるのが楽しくてインフィル印刷して遊んだ。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">ジャイロイドのインフィル <a href="https://t.co/ysvhxUgHNk">pic.twitter.com/ysvhxUgHNk</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1270992165011742721?ref_src=twsrc%5Etfw">June 11, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">場所ごとにインフィル変えられるの初めて知った <a href="https://t.co/o2SOWkIfA6">pic.twitter.com/o2SOWkIfA6</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1273537200689311744?ref_src=twsrc%5Etfw">June 18, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

QIDI X-Plusの最初の実用的な印刷は工具掛けの作成。

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">にぎやかになってきた工具掛け <a href="https://t.co/3K6EHd5E3M">pic.twitter.com/3K6EHd5E3M</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1272523713288830978?ref_src=twsrc%5Etfw">June 15, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">スライサーの設定デフォルトだけどだいぶいいんじゃないか <a href="https://t.co/u9JZ5w2Xaq">pic.twitter.com/u9JZ5w2Xaq</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1270944566523256832?ref_src=twsrc%5Etfw">June 11, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


# おわりに
今回はもっと長く使えたらいいな。

以上

