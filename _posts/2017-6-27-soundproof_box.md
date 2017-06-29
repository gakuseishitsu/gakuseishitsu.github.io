---

layout: post

title: CNCフライスの防音箱

---

<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB6.JPG">

社会人になり, 給料をもらえるようになったので早速CNCフライスを購入した.  
購入したのは<a href="https://www.omiocnc.com/products/x4-series/x4-800l-usb.html">OMIOCNCのX4-800L</a>.  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB0.JPG">

<a href="http://www.originalmind.co.jp/products/kitmill_rd">ORIGINALMINDのもの</a>と迷ったが, 以下の理由からこちらに決定した. 

* 扱えるワークが大きい(270×390×105mm)  
* スピンドルが高出力(800W)  
* 4軸加工ができて旋盤と兼任できる  
* スペックのみで比較すると安い  

届いた品を見てみると品質にはだいぶ不安はあるが趣味でやってく分には十分である.  

早速切削してみたが予想通りうるさい. 寮暮らしのため防音箱を作ることにした.  

### 防音箱の設計

始めに防音箱の主材料を決めた. 遮音性能は質量で決まるらしく, 金属で作りたいと思ったが値段的に木材で妥協した.  
結局木材の中で密度の高いパーティクルボードで作ることにした. 比重は0.7くらい.  
厚さを決めなければいけない. 遮音性能は次式できまるそうだ(<a href="http://park1.wakwak.com/~are/annoise/sound/oto-s2.html">あやしい出典</a>).  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/M1.JPG">

CNCフライスは自分のよく使う条件(15000rpm = 250Hz)で使っているときにだいたい72dBくらいの騒音を出していた.  
住宅地では45dB以下なら騒音にはならないそうだ(<a href="https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q1113206531">あやしい出典</a>). どれくらいの厚さがあれば72db - 45db = 27db遮音できるか計算してみた.  

| 厚さ mm | 面密度 kg/m^2 | 250Hzの遮音特性 dB |
|-----------:|------------:|:------------:|
| 10     |      7.0 |    22.3    |
| 15       |        10.5 |     25.9     |
| 20         |          14.0 |      28.4      |
| 25       |       17.5 |    30.3    |

表から20mmあれば十分遮音できそうである. 遮音は音を反射させてるだけでエネルギーを消してないから実際にはこれに加えて適当な吸音材を内側に貼らないといけないようである.  

主材料が決まったので設計した.  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/CAD1.jpg">

<img src="https://gakuseishitsu.github.io/images/soundproof_box/CAD2.jpg">

基本的にCNCフライスを覆ってるだけのなので素直に直方体形状. 覗き穴も設けた1.  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/CAD3.jpg">

パーツ単位でみるとこんな感じ.  

### 防音箱の製造

<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB1.JPG">

設計もできたので早速木材を発注した. 4日ぐらいで届いた.  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB2.JPG">

木材を手で加工. 久しぶりにのこぎりとか使った.  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB3.JPG">
<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB4.JPG">
<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB5.JPG">

釘打ち+ボンド止め. 蝶番もつけて出来上がったのが最初の写真.  

<img src="https://gakuseishitsu.github.io/images/soundproof_box/SB7.JPG">

吸音材貼って, 申し訳程度の安全対策を施し完成. ちゃんと騒音は減ってる(測ってない).  
次時間ができたら集塵システムの構築かな.  

以上