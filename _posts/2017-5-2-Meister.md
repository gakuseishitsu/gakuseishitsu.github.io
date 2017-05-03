---

layout: post

title: 鳥人間サークルで作ったもの

---

<img src="https://gakuseishitsu.github.io/images/meister_2013.jpg">

大学に入って, 最初に取り組んだのは人力飛行機作り (写真は執行代の機体).  
以下の部分を作っていた.  

* 計測機器 : プロペラの回転計など飛んでいる飛行機の状態を計測する機器
* 表示機器 : 計測機器の状態をパイロットがリアルタイムで確認するための表示機器
* 操縦系統 : 飛行機が進行方法や姿勢を変更するための尾翼の回転機構や制御機器

## 回転計

<img src="https://gakuseishitsu.github.io/images/rotation_sensor.jpg">
<img src="https://gakuseishitsu.github.io/images/rotation_sensor2.jpg">

回転計とは, 人力飛行機のプロペラの回転速度を計測する機器である(大学入って最初に作ったものなのに写真がない...).  

プロペラに回転を伝えるドライブシャフトにスリットの入った円盤が取り付けられシャフトとともに回転している. 機体に固定されたフォトインタラプタからは, シャフトの回転状態によって2種類の信号がパルスとなって送られる. そのパルスの幅をマイコンで計測することによって回転速度が計算できる. マイコンによって定期的に計測・計算された回転速度情報はシステムバスに送信される.  

回転を計測する方法には他にも磁気センサを用いるものや画像を使うものなどいろいろあったが, ひとまず先輩の真似事という理由で光式にした記憶がある. 簡単に回転速度を図れる方式ではあるが, 鳥人間では強い太陽光環境で使用するので遮光対策が必要になるというデメリットがあった気がする.  

## 表示機器

<img src="https://gakuseishitsu.github.io/images/meister_disp0.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp1.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp2.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp3.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp4.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp_concept.jpg">

表示機器とは, 飛んでる機体の状態をパイロットがリアルタイムで確認するための機器である.  

自分のいたサークルでは, 飛行機の高度, 対気速度, プロペラの回転速度, GPS座標を確認できるような表示機器を作った. 試作機も合わせて全部で4つも作ってしまった.  

基本的にはシステムバスから情報をもらって表示するだけなので特にソフトウェア的に高度なことはしていない. 構造は発砲スチロールをエポキシ樹脂で補強したような部材を用いた. 機器を取り付ける部分については発泡材では弱いため, 写真の通りアクリルやMDFを介している. 5枚目の写真が実際に機体に取り付けた状態である.  

### GPS表示器

<img src="https://gakuseishitsu.github.io/images/meister_disp5.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_gps.jpg">

GPS表示器とは, 表示機器の中で現在のGPS座標をパイロットに知らせるものである.  

GPS受信モジュールから座標情報をもらって, 液晶に地図と座標をプロットするのとともに, 受け取った情報をシステムバスに送るというものを作った. 生の液晶モジュールの制御は機械系の自分には厳しいが, 世の中には液晶コントローラ付きの液晶モジュールというものが秋葉あたりで売られていて, SPI等でつないでコマンドを送るだけで簡単にマイコンで液晶をいじることができ, 特に苦労はなかった.

画像は, 試作機のもので, 大学構内をまわって正しくっプロットできているか確認した時の写真である.

## 操縦系統

<img src="https://gakuseishitsu.github.io/images/meister_control1.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_control2.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_control3.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_control4.jpg">

操縦系統とは, 飛行機が進行方法や姿勢を変更するための尾翼の回転機構や制御機器である.  

パイロットがジョイスティックを動かすと, 電気的に尾翼が動くようになっている. CFRPやすって工作するのは非常に楽しかった.  