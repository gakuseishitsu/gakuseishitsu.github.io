---

layout: post

title: スピーカアンプのシャシ

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d1.JPG">

# はじめに
昔作ったスピーカアンプが壊れた.  
直してまた使ってもいいんだけどせっかくだから何か新しい試みをしようと思った.  
せっかく最近切削が楽しいので新しいCAMのパスの練習がしてみたいと考えていた.  
ということで既製品のアンプ基盤に切削でシャシを作ることにした.  

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">作ってから９年位動いてたアンプ、とうとう音が出なくなった、超久しぶりに中開けたけど配線やばい、今までよくショートしなかった <a href="https://t.co/tKuNWRKanv">pic.twitter.com/tKuNWRKanv</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1490219571898650625?ref_src=twsrc%5Etfw">February 6, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


# 使うアンプ
自分のマシンの加工領域も考えてコンパクトなスピーカアンプ基板を探して[このアンプ](https://bispa.co.jp/719)に決めた.  
早速シャシを設計するためにモデリングした. Fusion360でちょちょい.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d2.png">

周辺部品もモデリングしていい感じに配置.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d3.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d4.png">

最終的に↓のような感じに落ち着いた.  
思ったより幅が有ったのでスピーカ端子側は詰めた.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d5.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d6.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d7.png">

そして今回新しいCAMパスで遊ぶためにうねうねの3次元曲面を裏側に設けた.  
建前は自然体流の放熱面積を増やすことだけど実際10Wアンプなのでほぼ無用ではある.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d8.png">

レンダリングもしてみた.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d9.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d10.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d11.png">

# 3D曲面の加工
早速曲面側の加工を行った. 趣味としては初めてこんなでかいワーク買った (112 x 74 x t30).  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d21.JPG">

外形の輪郭加工を行ったのちにまずは荒加工. 3D負荷制御のパス.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d22.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d23.JPG">

そしてボールエンドミルでの仕上げ加工. スパイラスの仕上げパスを使ってみた.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d24.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d25.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d26.JPG">

いい感じに仕上がって満足である.  
反省点はスパイラルのパス全ての面を一度にやろうとすると, 山あり谷ありな面ではダウンカット/アップカット両方の面が現れてしまったこと. 確かに山の面と谷の面では表面の綺麗さが違ってた.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d28.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d29.JPG">

# 残りの加工
後はもう普通の2D加工.  
過去最高の切削体積で切子の積もり方がすごかった. 掃除機パンクした.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d30.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d31.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d32.JPG">

# 電気アセンブリ
タップ切ったり、カバーのアクリル削って作ったりしたのち基板締結してはんだ付け.  
配線もモデリングしていたので効率的にできた.  
そして無事通電確認して完成.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d33.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d34.JPG">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/220311_classD_amp/d35.JPG">

# おわりに
切削楽しかった. 音も無事鳴って一安心. LEDがちょっとまぶしすぎた.    

以上  