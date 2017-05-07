---

layout: post

title: 自動カメラ水平器

---

<img src="https://gakuseishitsu.github.io/images/stabilizer/stabilizer.jpg">

サークルでIMUやサーボモータをいじってたことから, なにか応用して遊べないかと思って作ろうと思った.  

システムとしては非常に単純である. 3軸の加速度センサとジャイロセンサの値から姿勢を計算してロールとピッチが0度になるようにP制御だかPI制御だかをかけて中央の円盤が常に水平を保とうとするようになっている.  計算方法については<a href="https://github.com/gakuseishitsu/ExtendedKalmanFilterForIMU">ここ</a>にまとめている.  

<img src="https://gakuseishitsu.github.io/images/stabilizer/stab2.jpg">