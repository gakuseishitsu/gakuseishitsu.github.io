# SysML TIPS

## Systems Engineeringの標準プロセス
システムズエンジニアリングは対象にあったプロセスに従って実施していく  
どのプロセスも大まかには「要求分析」⇒「アーキテクチャ設計」を行う  
世界標準のプロセスは以下三つ
 * ISO/IEC15288: 広い範囲をカバー
 * ANSI/EIA-632: 中くらいをカバー
 * IEEE1220: 開発のみをカバーしているが詳細度が高い

 さらにSysMLを使ったMBSEを行う汎用プロセスは以下が有名  
 * OOSEM（Object-Oriented Systems Engineering Method）
   * INCOSEの提供するMBSEプロセス
   * 「システムズモデリング言語SysML」で紹介
 * SYSMOD（SYStems MODeling process）
   * 「 SysML/UMLによるシステムエンジニアリング入門」で紹介
 * Harmony for Systems Engineering
   * IBM社の提供するMBSEプロセス

JAXAでは[ここ](https://ssl.tksc.jaxa.jp/isasse01/kanren/BDB/BDB06007BSEkihon.pdf)に示すようなシステムズエンジニアリングプロセスを設定してる。

趣味のものつくりの為に自分用のエンジニアリングプロセスを設定する!　　

---
## SysMLのダイアグラム
UMLでは13個だったのがSysMLでは9個  
UMLはソフトウェアの詳細設計フェーズでも使用するのに対してSysMLは概念検討までしか使わないから少ないダイアグラムでもよい  
SysML特有なのは要求図とパラメトリック図  

<img src="https://www.ogis-ri.co.jp/otc/hiroba/technical/SysEngSysML/img/fig105.png">

---
## どのプロセスでどのダイアグラムを使うか
 ISO/IEC15288 (JIS X0170)のプロセスと使えるダイアグラムの一覧  
<img src="https://www.ogis-ri.co.jp/otc/hiroba/technical/SysEngSysML/img/tab101.png">

趣味のものつくりでは利害関係者要求定義プロセスはいらなさそう  

参考文献でのプロセスを以下アクティビティー図で示す。
```plantuml
@startuml
partition "参考文献でのシステムズエンジニアリングプロセス" {
start
:要求分析(サービスレベル);
:要求分析(システムレベル);
:方式決定;
stop
}
@enduml
```
```plantuml
@startuml
partition "方針決定" {
start
:振る舞いの検討;
:仕様の詳細化;
:内部構造の検討;
:論理構造の物理構造へのマッピング;
:パフォーマンス分析;
:構造の確定;
:ユースケースの検証;
stop
}
@enduml
```
---

## サービスレベル要求分析
```plantuml
@startuml
partition "サービスレベル要求分析" {
start
:ユースケース分析;
:非機能的要求検討;
:コンテキスト図作成;
stop
}
@enduml
```
### 1. ユースケース分析
```plantuml
@startuml
frame サービスレベルユースケース {
  組込み機器開発者 -- (システムズエンジニアリングを経験する)
}
@enduml
```
楕円がユースケースで、システム外部から識別できる機能単位で記述します。 よく内部処理の単位でユースケースが書かれている例を見ますが、これは間違いです。 外部から識別できる機能に着目します。
人型をしている図形はアクターと呼ばれ、システムのステークホルダ (利害関係者) を表します。
### 2. 非機能的要求検討

```plantuml
@startuml

hide circle
hide empty members
hide method

!define REQ1 "主要求"
!define REQ2 "実現可能性"
!define REQ3 "コスト"
!define REQ4 "利用部品"
!define REQ5 "利用部品"
!define REQ6 "利用部品"
!define REQ7 "手段"

!definelong req(name,txt,label)
class "name" as label <<requirement>> {
Text=txt
}
!enddefinelong

!definelong freq(name,txt,label)
class "name" as label <<functionalRequirement>> {
Text=txt
}
!enddefinelong

!definelong dcnstr(name,txt,label)
class "name" as label <<designConstraint>> {
Text=txt
}
!enddefinelong

!define nest(x,y) x +-- y
!define derive(x,y) x <.. y : <<deriveReqt>>
!define refine(x,y) x <.. y : <<refine>>
!define derivel(x,y) x <.. y : <<deriveReqt>> link


title 図5 サービスレベル要求図

package "req サービス要求" <<Frame>> {
    req(REQ1,システムエンジニアリングを経験する,A1)
    freq(REQ2,ハードウェアを含めて実現可能である,A2)
    dcnstr(REQ3,なるべくコストをかけない,A3)
    dcnstr(REQ4,使える既存システムは流用する,A4)
    dcnstr(REQ5,CPLDを利用する,A5)
    dcnstr(REQ6,既存の電光掲示板システムを流用する,A6)
    req(REQ7,電光掲示板をCPLD駆動に変更する,A7)
    note "allocatedFrom\n<<useCase>>システムエンジニアリングを経験する" as N2
}

nest(A1,A2)
nest(A1,A3)
nest(A1,A4)

derive(A2,A5)
note top on link : <<rationale>>\nCPLDならハードウェア\n回路の変更が容易
derive(A3,A5)
derive(A3,A6)
derive(A4,A6)
derive(A5,A7)
derive(A6,A7)

refine(A1,A7)

N2 .. A1

@enduml
```
要求図は UML には存在しない SysML 独自のダイアグラムで、非機能的要求を含めた要求を記述するために用いられます。
要求は複数の要求の集合として表すことができ、ネストを用いて表現します。 要求にはさまざまな種類があり、ユーザが独自にステレオタイプ requirement を拡張しても良いことになっています。
要求は機能要求 (functionalRequirement)、設計制約 (designConstraint) から検討される
派生要求は(deriveReqt)で表す 
元の要求を洗練する場合は (refine) する

### 3. コンテキスト図作成
⇒SYSMLでは定義されていない。1.2で定めたものを明確化しただけ

---

## システムレベル要求分析

```plantuml
@startuml
partition "システムレベル要求分析" {
start
:ユースケース分析;
partition "非機能的要求検討"{
  :判明している要求の確認;
  :利用予定ハードウェアの調査;
  :要求の明確化;
}
stop
}
@enduml
```

### 1.ユースケース分析
```plantuml
@startuml

skinparam monochrome true

frame サービスレベルユースケース {
  left to right direction
  skinparam packageStyle rectangle
  actor 文字列入力装置
  actor 利用者
  rectangle 電光掲示板 {
    文字列入力装置 -- (表示する文字列を設定する)
    利用者 -- (文字列を表示する)
    (スクロールする) .> (文字列を表示する) : <<extend>>
  }
}
@enduml
```

### 2.非機能的要求検討
```plantuml
@startuml

skinparam monochrome true

hide circle
hide empty members

package "bdd 論理構成階層構造" <<Frame>> {
class 電光掲示板 <<block >>
class 通信ユニット <<block >>
class グラフィック生成ユニット <<block >>
class ドット列情報 <<data Type>>
class 表示器制御ユニット <<block >>
class フォント <<data Type >>
class グラフィックジェネレータ <<block >>
class スクロール制御 <<block >>
class 表示コントローラ <<block >>
class "Matrix LED" <<block >>
}

電光掲示板 *-- 通信ユニット
電光掲示板 *-- グラフィック生成ユニット
電光掲示板 *-- ドット列情報
電光掲示板 *-- 表示器制御ユニット
グラフィック生成ユニット *-- フォント
グラフィック生成ユニット *-- グラフィックジェネレータ
グラフィック生成ユニット *-- スクロール制御
表示器制御ユニット *-- 表示コントローラ
表示器制御ユニット *-- "Matrix LED"

@enduml
```


---