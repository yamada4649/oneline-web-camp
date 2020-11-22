# Flexbox(Flexレイアウト)を学ぼう

## 課題概要
 - 確認問題 : 4問
 - 演習課題 : 1問
---

## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。

### 問１
以下のうち、旧レイアウト方法の特徴**ではない**ものはどれでしょう。
- a. これまではHTMLのレイアウトの主流だった
- b. 仕組みや使い方が複雑でわかりにくい
- c. floatは高さが消えるため、clearfixが必要
- d. 縦方向の整列が得意

<details>
<summary>解答はこちら</summary>

#### 解答
【d】

#### 解説
**旧レイアウト方法の欠点**<br>
これまでのHTML・CSSでは`float: left/right;`と`margin:0 auto;`を使用してブロック要素をレイアウトする方法が主流でした。<br>
しかしこれには「仕組みや使い方が複雑でわかりにくい」「floatは高さが消えるため、clearfixによる解除が必要」などの欠点がありました。<br>
またその他にも特に、floatやmarginは横方向の位置を指定するプロパティであるため、縦方向の整列に弱いという欠点がありました。
</details>

### 問２
以下のうち、Flexレイアウトの特徴**ではない**ものはどれでしょう。（複数）
- a. 上下左右に簡単にレイアウト可能
- b. HTMLソースはそのままに、CSSのみで順序を入れ替え可能
- c. 新旧あらゆるブラウザで正常に動作可能
- d. 高さが消えるため、clearfixが必要
- e. 中央寄せ、均等分布などの整列を簡単に実現可能
- f. 親や子の箱のサイズが拡大縮小しても、その空間に応じて柔軟性高くレイアウトが可変する

<details>
<summary>解答はこちら</summary>

#### 解答
【c】,【d】

#### 解説
**Flexレイアウトの利点と注意点**<br>
Flexレイアウトはこれまでの方法の欠点を解消し、レイアウトを簡単にコーディングできる新しい仕組みです。<br>
特に、floatの特性である「高さの消失」や「それに伴うclearfixの使用」などがないため、直感的にわかりやすくコーディングを行うことが可能です。<br>
反面、比較的新しいプロパティであるため、古い環境には対応していなかったり、一部ブラウザ（IE系）では動作が不安定だったりする注意点があります。
</details>

### 問３
Flexレイアウトの基本的な使用方法は次のうちどれでしょう。
- a. 親の箱に float: left/right; のプロパティを指定する
- b. 子要素に float: left/right; のプロパティを指定する
- c. 親の箱に display: flex; のプロパティを指定する
- d. 子要素に display: flex; のプロパティを指定する
- e. 親の箱に flex: 1; のプロパティを指定する
- f. 子要素に flex: 1; のプロパティを指定する

<details>
<summary>解答はこちら</summary>

#### 解答
【c】

#### 解説
**整列させたい要素の"親"に指定する**<br>
display: flex;は、floatやmarginのように移動させたい要素自体ではなく、それを囲む"親"の箱に指定します。<br>
要素自体に指定しても意図した動作とならないため、注意が必要です。<br>
display:flexを指定した箱はFlexコンテナーとなり、内容のレイアウトを指定することができるようになります。<br>
flex:xx; というまぎらわしいプロパティがありますが、これはFlexコンテナー内でFlexアイテムに対して使用する全く別のプロパティであるため、混乱しないように注意しましょう。
</details>

### 問４
Flexレイアウトで図のような表示を作成したい場合、正しいスタイルの記述方法は次の内どちらでしょう。<br>
<img src="https://wals.s3-ap-northeast-1.amazonaws.com/uploads/carriculum/1193/flex19.png">
- a.
【CSSファイル】
```css
.flex {
  color: #fff;
  background-color: #00c7ce;
  width: 300px;
  height : 150px;
  display: flex;
  justify-content: center;
  align-items : center
}
```
- b.
【CSSファイル】
```css
.flex {
  color: #fff;
  background-color: #00c7ce;
  width: 300px;
  height : 150px;
  display: flex;
  flex-direction: row;
  align-content: center;
}
```
<details>
<summary>解答はこちら</summary>

#### 解答
【a】

#### 解説
**HTMLファイルとCSSファイルの紐付け**<br>
横方向の中央に内容を整列する際には`justify-content: center;`を、<br>
縦方向の中央に内容を整列する際には`align-items: center;`を使用するため、正解は【a】です。<br>
bの`flex-direction: row;` はFlexコンテナーの内容を横方向に並べる指定、<br>
`align-content: center;` はFlexコンテナーの内容が複数行のときに縦方向の中央に内容を整列する指定であるため、誤りです。
</details>

---
## 演習課題
### 演習1
#### 課題クリア条件
- [ ] Pull Request形式で提出すればクリア

#### 内容
HTMLファイルとCSSファイルを作成し、以下を参考にWebページを作ってみましょう。<br>
※リセットCSSを適用すること。

<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90333480-09123a00-e001-11ea-8b3a-2aef42b6b429.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90333488-162f2900-e001-11ea-8d2c-08158e2c81d6.png" alt="guide.png">
</details>

#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `flex_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [flex/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[flex/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
