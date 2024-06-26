# 事前に準備するもの
## reset.css
デフォルトのスタイルをリセットするcss。
ブラウザの進化に合わせて定期的に新しいものが出るのでその度に良さそうなやつを入れる。
<br />
<br />
<br />

# 命名規則
BEMを利用する。  
https://getbem.com/
<br />
<br />
<br />

## 外側のものを命名しない
基本的にBEM自体がより内側のものに詳細なクラスを付与していく手法なので、  
`outer`や`wrapper`といった自分より外側のものを定義する名前は利用しない。
<br />
<br />
<br />

## 方向や位置を命名しない
Web開発ではデザイナーとの綿密な協議の中でデザイン変更が発生することがしばしばある。  
`footer__left`や`main__center`などを利用すると、デザイン変更のたびに直す必要が発生する。  
<br />
<br />
<br />

## idはJS以外で極力使わない。
idをcssで指定すると、BEM記法でのスタイリングが難しくなる。  
できれば避けるべき。  
<br />
<br />
<br />

## 変数
変数は_variable.scssに書く。  
<br />
<br />
<br />

## 命名規則リスト
書いていないものはよしなに。  
基本的には省略せず単語で。  
省略形でも通じるような言葉は省略形で良い

### Block単位
- container
  - 要素を入れる大きめのBlock
- content
  - container内部の要素
- section
  - ブログなど文字媒体において段落、章で分割する区切り
- block
  - 文字媒体以外の区切り
- inner
  - 何かの内部。よく使いがち。特に当てはまらなければこれで。

<br />
<br />
<br />

### Element単位
- nav
  - ナビゲーション
- outline
  - 目次
- list
  - リスト要素
- link
  - リンク要素
- item
  - リスト内部orリスト以外で並んでいる項目
- detail
  - 詳細
- title
  - タイトル
- text
  - テキスト
- lead
  - リード文
- kv
  - キービジュアル
- menu
  - メニュー
- box
  - 小さい箱、中に別の要素が入る
- overlay
  - 被せる要素

### Modifier
- active
  - 活性化されているもの
- deactive
  - 非活性なもの
- enable
  - 利用できる要素（activeとちかい）
- current
  - 現在選択されている要素（selectedでも良さそう）
- color
  - red, greenなど色指定
- 数字
  - 連番で何番目の要素（できるだけ使わずcssのnthで対応）
  
<br />
<br />
<br />

## 例外
bodyに対する指定はindex.scssの@useの下に入れていく。  
量が多い場合は（ほぼありえないし、その状況なら適切にBEM記法で書いた方がよいが）  
_base.scssなどにうつす。