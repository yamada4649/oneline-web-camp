# 5章【ヘッダーとフッターを作ろう】

## 課題概要
 - 継続課題 : 1問
 - 確認問題 : 3問
 - 演習課題 : 1問

---
## 継続課題
教科書を読み進める前に、以下の準備を行いましょう。

1. ご自身のPC内のローカルリポジトリでの作業
   1. まず、ターミナル（WindowsはGit Bash）上でご自身のPC内のローカルリポジトリに移動して下さい。
   1. `git pull`をして下さい。
   1. `master`Branchに移動して下さい。
      1. `git checkout master`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`master`Branchであれば良い。
   1. `continuous_exercise_05`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_05`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_05`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行いましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_05`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_05`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---

## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問１
3番目に重要な見出しを表すタグは、何タグですか。

<details>
<summary>解答はこちら</summary>

#### 解答
【h3タグ】

#### 解説
<b>見出しを表すタグ</b><br>
見出しは英語では"headline"ないし"heading"と言われます。<br>
その頭文字をとって、見出しは`<h>`に1~6の順番が付いたものとなっています。<br>
1が1番大きい見出し、6が1番小さい見出しです。使い分けていきましょう。
</details>

### 問２
ブロック要素の特徴として、正しいものは次のうちどれでしょう。
- a. 横並びになる
- b. 上下に余白ができない
- c. 幅と高さが指定できる

<details>
<summary>解答はこちら</summary>

#### 解答
【c】

#### 解説
**ブロック要素の特徴**<br>
a. はインライン要素、インラインブロック要素の特徴です。<br>
b. はインライン要素の特徴です。
</details><br>

#### 問３
以下の要件に従って、Webページを作ってください。
【要件】<br>
1. headerタグ、h1タグ、navタグ、olタグ、liタグを用い、headerタグの中にh1タグとnavタグがあり、navタグの中にolタグ、olタグの中にliタグが4つある構成にする
2. h1タグの中身は、EXAMPLE とする
3. liタグの中身は、それぞれMENU1、MENU2、MENU3、MENU4 とする
4. class名は、それぞれ"headline"、"nav"、"list"、"list-item"とする
5. headerのwidth（横幅）は、10％にする
6. headlineのfont-size（文字の大きさ）は、22pxにする
7. nav内の文字を中央寄せ（text-align）にする
8. "list"クラスにはcssでpadding-left: 40px;を適用させる

※リセットCSSの適用でブラウザがデフォルトで持っているcssを打ち消したことで、olの番号が表示される領域が消えてしまったことを補うため<br>
【完成図】
<img src="https://wals.s3-ap-northeast-1.amazonaws.com/curriculum/htmlcss/kakunin5.png">

<details>
<summary>解答はこちら</summary>

#### 解答
HTML/CSSはこちら<br>
【index.html】
```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <link rel="stylesheet" href="style.css" />
    <title>EXAMPLE</title>
  </head>

  <body>
  <header>
    <h1 class="headline">EXAMPLE</h1>
    <nav class="nav">
      <ol class="list">
        <li class="list-item">MENU1</li>
        <li class="list-item">MENU2</li>
        <li class="list-item">MENU3</li>
        <li class="list-item">MENU4</li>
      </ol>
    </nav>
  </header>
  </body>
</html>
```

【style.css】
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
header {
  width: 10%;
}
.headline {
  font-size: 22px;
}
nav {
  text-align: center;
}
.list{
  padding-left: 40px;
}
```
#### 解説
まずは1の要件を元にHTMLを記述していきます。<br>
【index.html】
```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <title>EXAMPLE</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header>
      <h1></h1>
      <nav>
        <ol>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
        </ol>
      </nav>
    </header>
  </body>
</html>
```
次に2、3に沿ってHTMLそれぞれの要素に文字を追加します。<br>
【index.html】
```html
<header>
  <h1>EXAMPLE</h1>
  <nav>
    <ol>
      <li>MENU1</li>
      <li>MENU2</li>
      <li>MENU3</li>
      <li>MENU4</li>
    </ol>
  </nav>
</header>
```
続いて4でclass属性と属性値を割り振ります。<br>
【index.html】
```html
<header>
  <h1 class="headline">EXAMPLE</h1>
  <nav class="nav">
    <ol class="list">
      <li class="list-item">MENU1</li>
      <li class="list-item">MENU2</li>
      <li class="list-item">MENU3</li>
      <li class="list-item">MENU4</li>
    </ol>
  </nav>
</header>
```
ここまででHTMLの記述は終了です。<br>
続いて5の要件からCSSの記述に移ります。<br>
【style.css】
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
header {
  width: 10%;
}
```
最後に6、7、8の要件をCSSに記述し、完成図通りになればクリアです。<br>
【style.css】
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
header {
  width: 10%;
}
/* 以下を追加 */
.headline {
  font-size: 22px;
}
nav {
  text-align: center;
}
.list{
  padding-left: 40px;
}
```
</details>


---
## 演習課題
### 演習1
#### 課題クリア条件
- [ ] Pull Request形式で提出すればクリア

#### 内容
HTMLファイルとCSSファイルを作成し、以下を参考にWebページを作ってみましょう。<br>
ヒント：Flexboxでflex-wrapというプロパティ、wrapという値を利用します。

<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90330008-84b1be00-dfe4-11ea-9f1c-73cb13e68a9c.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90330009-87141800-dfe4-11ea-9709-b0b332e14a31.png" alt="guide.png">
</details>

<details>
<summary>カラーコード(colorcode.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90330016-9d21d880-dfe4-11ea-8d17-c66c96ee40ce.png" alt="colorcode.png">
</details>

#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `05_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [05/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[04/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
