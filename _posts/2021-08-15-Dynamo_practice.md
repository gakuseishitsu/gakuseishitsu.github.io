---

layout: post

title: Dynamoで曲面にアイソグリッド構造生やしてみた

---

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di1.png">

# はじめに
Fusion360等の3DCADでは通常曲面にスケッチを書くことや曲面上の閉じた曲線の法線方向の押し出し操作をすることができない. (シートメタルの機能を使って無理やりそれっぽいことはできるけど)  
一方3DCG系のソフトではUV座標の操作は普通に行える. 

機械設計でUV座標の操作が必要なモデリング対象はそんなにおおくないと思っているが、例えば戦闘機のジェットエンジンの円筒テーパー部のアイソグリッド構造なんかはUV座標操作ができたら簡単にモデリングできるんだろうな～なんて思うことはあった.  

ということで今回モデリングの表現の幅を広げるためにUV座業の操作ができるモデリングソフトに入門しようと考えた.  機械系CADと親和性が高くてコンピューテーショナルデザイン的なことができるもので有名なものはRhinoceros+Grasshopperで(多分?)、情報も多くありそうだからそちらで入門したかったがAutodesk系ソフトと親和性が高いのはDynamoなので今回はそっちで入門してみた(DynamoできるようになればGrasshopperもすぐに同じレベルになれると信じてる).  

(Fusion360やInventorでもAPIレベルならUV座業のマッピングはできるようだが今回はパス)   

# Dynamo入門
<a href="https://primer.dynamobim.org/ja/">公式の入門コース</a> を一通り終えて、万能感が残ってるうちに何かしら手を動かして定着させようと思った.  
最初に目的であるUV座標の取り扱いに慣れるため、曲面に曲線を書いて厚みを付けてみた.  
直接曲面に書き込むのではなく通常の座標に曲線を書いて、それを曲面上にマッピングする.  簡単!  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di2.png">


# 曲面にアイソグリッド構造を生やしてみる
引き続き本番のアイソグリッド構造の実装をやってみた.  
Fusion360で作成した曲面をSATファイルに変換して、Dynamoで取り込んで実装. 良い頭の体操になった.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di3.png">


<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di4.png">

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di5.png">


# 中身
自分用の記録なので他の人のためになるような細かい話はしないが, 流れだけ説明.  
中身の全体像は↓のような感じ, ビジュアルプログラミングは出来上がったスパゲッティ(コード)を見て謎の満足感がある.  

<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di11.png">

1. 基準座標の設定
2. Fusion360から曲面のインポート
3. 基準座標にスケッチ (縦ライン、斜めライン)
4. スケッチを曲面上ににマッピングして厚みづけ
5. 元曲面に厚みを付ける
6. ボディがたくさんあるので1つに統合
7. 交差部にフィレットを設ける処理
8. フィレットをかける線分が正しく抽出されているかのチェック
9. 円筒穴の実装
10. 出来上がったボディのSATファイルへの出力

前半部分
<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di7.png">

マッピングする前の線たちと出来上がったボディ
<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di8.png">

後半部分
<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di9.png">

地味に大変だったフィレット. 全てのエッジの中からフィレットをかけるエッジだけフィルタして確認するのは面倒だった. ↓は可視化して正しく必要なエッジが抽出できたかのチェック.  
<img src="https://raw.githubusercontent.com/gakuseishitsu/gakuseishitsu.github.io/master/images/210815_dynamo_isogrid/di10.png">

# おわりに
今回はUV座標のモデリング能力の獲得のためDynamo習得したが、次はRevit(BIM)との連携も習得したい.   

以上  

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">フィレットと円孔つけられた. とても重たい. <a href="https://t.co/YeXXLxbmo5">pic.twitter.com/YeXXLxbmo5</a></p>&mdash; がくせいしつ (@YASUBE_T_AU) <a href="https://twitter.com/YASUBE_T_AU/status/1426778752919375873?ref_src=twsrc%5Etfw">August 15, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>