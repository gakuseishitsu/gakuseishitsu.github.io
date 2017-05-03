---

layout: post

title: 鳥人間サークルで作ったもの

---

# 人力飛行機

<img src="https://gakuseishitsu.github.io/images/meister_2013.jpg">

大学に入って, 最初に取り組んだのは人力飛行機作り (写真は執行代の機体).  
以下の部分を作っていた.  

* 計測機器 : プロペラの回転計など飛んでいる飛行機の状態を計測する機器
* 表示機器 : 計測機器の状態をパイロットがリアルタイムで確認するための表示機器
* 操縦系統 : 飛行機が進行方法や姿勢を変更するための尾翼の回転機構や制御機器
* システム : 電装・操舵のコンポーネントとそれらのインターフェースを含めたシステム全体
* その他 : サークル所属中に遊びで作ったもの

## 計測機器

### 回転計

<img src="https://gakuseishitsu.github.io/images/rotation_sensor.jpg">
<img src="https://gakuseishitsu.github.io/images/rotation_sensor2.jpg">

回転計とは, 人力飛行機のプロペラの回転速度を計測する機器である(大学入って最初に作ったものなのに写真がない...).  

プロペラに回転を伝えるドライブシャフトにスリットの入った円盤が取り付けられシャフトとともに回転している. 機体に固定されたフォトインタラプタからは, シャフトの回転状態によって2種類の信号がパルスとなって送られる. そのパルスの幅をマイコンで計測することによって回転速度が計算できる. マイコンによって定期的に計測・計算された回転速度情報はシステムバスに送信される.  

回転を計測する方法には他にも磁気センサを用いるものや画像を使うものなどいろいろあったが, ひとまず先輩の真似事という理由で光式にした記憶がある. 簡単に回転速度を図れる方式ではあるが, 鳥人間では強い太陽光環境で使用するので遮光対策が必要になるというデメリットがあった気がする.  

使用言語 : C言語  
要した知識 : 基板CAD, 基板加工, 機械CAD, レーザ加工, 組み込みの知識

## 表示機器

<img src="https://gakuseishitsu.github.io/images/meister_disp1.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp2.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp3.jpg">
<img src="https://gakuseishitsu.github.io/images/meister_disp4.jpg">

### GPS表示器

<img src="https://gakuseishitsu.github.io/images/meister_disp5.jpg">

## 操縦系統

### 尾翼機構

### 尾翼制御機器

## システム

## その他

### 看板

### 眼鏡埋め込み式表示器