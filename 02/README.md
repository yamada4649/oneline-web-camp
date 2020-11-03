# 2章【HTML・CSSの基本書式を学ぼう】

## 課題概要
 - 確認問題 : 5問
 - 演習課題 : 1問

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。

### 問１
Webページに表示させたい要素は、次のうちどちらに記入しますか。
- a. bodyタグ内
- b. headタグ内

<details>
<summary>解答はこちら</summary>

#### 解答
【a】

#### 解説
bodyタグ内には、Webページに表示させたい情報を記述します。<br>
ex) pタグ、h1タグ、imgタグなど<br>
一方、headタグ内には、Webページ自体の情報を記述します。<br>
headタグ内に記述された情報は、titleタグを除いては通常ブラウザ上に表示されません。<br>
ex) metaタグ、linkタグなど
</details>

### 問２
リンクを作成するために用いられるタグと属性は、次のうちどれでしょう。
- a. `<a src=""></a>`
- b. `<a content=""></a>`
- c. `<a href=""></a>`
- d. `<a lang=""></a>`

<details>
<summary>解答はこちら</summary>

#### 解答
【c】

#### 解説
**aタグ**<br>
aタグは"anchor"（船の錨）の略称で、リンクの出発点と到達点を指定するタグです。<br>
出発点はaタグを記述するHTMLファイル、到達点はhref属性の値です。<br>
aタグに囲まれた部分をクリックすると、href属性値に移動します。<br>
【htmlファイル例】<br>
```html
<a href="https://web-camp.io/">WebCampへのリンク</a>
<!-- 「WebCampへのリンク」という文字をクリックすると "https://web-camp.io/" に移動する -->
```
</details>

### 問３
文字化けを防ぐために使われる要素は、次のうちどれでしょう。
- a. `<meta charset="UTF-7">`
- b. `<meta charset="UTF-8">`
- c. `<meta name="description">`
- d. `<meta name="viewport">`

<details>
<summary>解答はこちら</summary>

#### 解答
【b】

#### 解説
**文字化けを防ぐ要素**
metaタグは、Webページの情報を定義するためのタグです。<br>
属性は様々なものを持ちますが、ここではcharset属性を使います。<br>
charsetは"character set"の略称で、日本語で言うところの「言語設定」という意味を持ちます。<br>
UTF-8属性値は文字コードと呼ばれるもので、コンピュータ上で文字を扱うために個々の文字、記号に割り当てられた固有の番号を指します。<br>
世界で最もポピュラーな文字コードですので、UTF-8だけはしっかりと覚えてください。
</details>

### 問４
HTMLとCSSファイルを関連付けるために必要な要素は、次のうちどれでしょう。
- a. `<link rel="stylesheet" href="">`
- b. `<link rel="stylesheet" src="">`
- c. `<css rel="stylesheet" href="">`
- d. `<css rel="stylesheet" src="">`

<details>
<summary>解答はこちら</summary>

#### 解答
【a】

#### 解説
**HTMLファイルとCSSファイルの紐付け**<br>
HTMLファイルと外部ファイルを紐付けるには、linkタグを用います。<br>
linkタグはheadタグ内に含まれます。<br>
主にCSSファイルとの紐付けに用いられる要素ですので、その用途は確実に覚えましょう。<br>
rel属性は現在の文書からみた、リンク先となるリソースの位置づけを表します。<br>
属性値がリソースを表すものなので、CSSをリンク先とする際の属性値は"stylesheet"となります。
</details>

### 問５
正しい記述は、次のうちどちらでしょう。
- a.
```html
<div id="content"></div>
<div id="content"></div>
<div id="content"></div>
```
- b.
```html
<div class="content"></div>
<div class="content"></div>
<div class="content"></div>
```

<details>
<summary>解答はこちら</summary>

#### 解答
【b】

#### 解説
**id属性とclass属性の使い分け**
id属性は、1つのWebページで同じ値を複数持つことができません。<br>
class属性は1つのWebページで同じ値を複数持つことができるので、今回のようなdivタグが3つ並び、同じスタイルを指定したいという場合にはclass属性をつけるのが適切です。
</details>

---
## 演習課題
### 演習１
#### 課題クリア条件
- [ ] Pull Request形式で提出すればクリア

#### 内容
HTMLファイルとCSSファイルを作成し、以下の画像を参考にWebページを作ってみましょう。<br>
「sample.png」が完成図、「guide.png」が演習の指示になります。

指示の箇所以外は、ご自身で決めて作られてかまいません。たとえば、今回のaタグの指示ではhrefで設定する内容はお任せいたします。<br>
以降の章における演習問題も同様です。

<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90329921-baa27280-dfe3-11ea-8b62-e3bb166accd9.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90329928-ca21bb80-dfe3-11ea-9d72-354e831bd8a4.png" alt="guide.png">
</details>


#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `02_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [02/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[02/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
