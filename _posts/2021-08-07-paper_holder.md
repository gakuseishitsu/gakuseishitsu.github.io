---

layout: post

title: ペーパーホルダ

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph1.png">

# はじめに
毎回キッチンペーパーを出し入れするのが面倒だったため磁石で吊るせるようにしたいと思った.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph0.jpg">

# 設計製造
そんなに大きな力がかかるわけでもないし、磁石と棒を適当に固定出来ればいいものだったが,  
面白い形状を期待してFusion360のGenerative Design回してみた.  

赤が障害物(形状が侵入できない部分)、緑が保持する部分(最適化の影響を受けない部分).  
その他条件は適当にそれっぽいものを入れた.

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph2.png">

最適化の過程.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph3.gif">

出てきた形状. 腕みたい.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph4.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph5.png">

生の出力データは微妙なところがたくさんあるのでT-スプラインを修正.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph6.png">

円筒部のクアッドメッシュがスパイラル上になっている部分があって、地味に修正が大変だった.  
力技で修正.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph7.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph8.png">

修正し終わった結果.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph9.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph10.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph11.png">

印刷.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph12.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210807_paper_holder/ph13.jpg">

完成. ちゃんと使える.  

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">ペーパーホルダ生成. Tスプラインの編集時間溶ける. <a href="https://t.co/6bVTxhcwdF">pic.twitter.com/6bVTxhcwdF</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1423806237813088268?ref_src=twsrc%5Etfw">August 7, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


# おわりに
結局Generative Designは出てきた結果を考察して1から設計したほうが良い.  

以上  