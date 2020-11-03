# 4章【Webページの枠組みを作ろう】

## 課題概要
 - 継続課題 : 1問
 - 確認問題 : 3問
 - 演習課題 : 1問

---
## 継続課題
本章以降、「CARAVAN」というWebサイトを作成していくために、「caravan」フォルダ内の「index.html」と「style.css」を随時変更していきます。<br>
その変更点をGitHub上で管理し、Pull Requestを送ることで、提出したと見なします。<br>
本章では以下の事を行って下さい。

1. ご自身のPC内のローカルリポジトリでの作業
   1. まず、ターミナル（WindowsはGit Bash）上でご自身のPC内のローカルリポジトリに移動して下さい。
   1. `git branch`で「現在、自分がどのBranchにいるか？」を確認して下さい。
      1. `*`が付いているBranchが現在自分がいるBranchです。
         1. `* master`となっていれば、「現在、自分は`master`Branchにいる」という事を意味します。
   1. `continuous_exercise_04`というBranchを作成して移動して下さい。
      1. `git branch "continuous_exercise_04"`というコマンドを打つとBranchを作成できます。
      1. `git branch`で「現在、自分がどのBranchにいるか？」を確認して下さい。
      1. 恐らく、現在地が`continuous_exercise_04`Branchではないと思いますので、移動して下さい。
         1. `git checkout "continuous_exercise_04"`というコマンドを打つと移動できます。
      1. `git branch`で「現在、自分がどのBranchにいるか？」を確認して下さい。
         1. `*`が`continuous_exercise_04`に付いていたら成功です。
	 1. ※ちなみに、 `git checkout -b "continuous_exercise_04"`というコマンドで「Branchの作成と移動」を一気に行うことが出来ます。
   1. 教科書内で作成した「caravan」フォルダを、本リポジトリの[continuous_exercise](../continuous_exercise)ディレクトリ(フォルダ)に移動する
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_04`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_04`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

**※以降、Branchの作成方法や移動方法などの詳細な説明は省略しますので、もし分からなくなったら、本コンテンツを参照下さい。**

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。

### 問１
Flexboxを利用する際、対象となる要素から見てどの要素にCSSを記載しますか。
- a. 親要素
- b. 子要素
- c. 孫要素

<details>
<summary>解答はこちら</summary>

#### 解答
【a】

#### 解説
Flexboxでは操作したい要素の親要素にCSSを記載します。
</details>

### 問２
「要素自身の中央揃え」は、次のどれでしょうか。
- a. margin: auto 0;
- b. padding: 0 auto;
- c. margin: 0 auto;
- d. padding: auto 0;

<details>
<summary>解答はこちら</summary>

#### 解答
【c】

#### 解説
**ボックスの中央寄せ**<br>
marginは値を4つ取ることができ、今回のように値が2つの場合は<br>
前の値が上下の margin 、後ろの値が左右の値となります。<br>
そのため、「上下に余白は取らず、左右のmarginを自動で半分に調節してください」<br>
という意味を持ちます。この意味によって、結果的に中央に寄ります。
</details>

### 問３
次の要件に従って、Webページを制作してください。<br>
（デスクトップにboxesというフォルダ、boxesフォルダにindex.html, style.cssを作成しましょう。）
1. `<div class="boxes">`要素の中に`<div class="box1">`要素と`<div class="box2">`が存在するようにHTMLを作成する
2. .boxes：横幅600px、背景色yellow、.boxesクラスそのものと子要素を両方中央寄せにする
3. .box1：横幅150px、高さ400px、背景色orange
4. .box2：横幅250px、高さ400px、背景色red

<details>
<summary>解答はこちら</summary>

#### 解答
HTML/CSSは以下の通りです。<br>
【index.html】
```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <title>boxes</title>
    <link rel="stylesheet" href="style.css" />
  </head>

  <body>
    <div class="boxes">
      <div class="box1"></div>
      <div class="box2"></div>
    </div>
  </body>
</html>
```

【style.css】
```css
.boxes {
  width: 600px;
  margin: 0 auto;
  background-color: yellow;
  display: flex;
  justify-content: center;
}

.box1 {
  width: 150px;
  height: 400px;
  background-color: orange;
}

.box2 {
  width: 250px;
  height: 400px;
  background-color: red;
}
```

#### 解説
完成図は以下のようになります。
<img src="https://wals.s3-ap-northeast-1.amazonaws.com/curriculum/htmlcss/kakunin4.png">
</details>

---
## 演習課題
### 演習1
#### 課題クリア条件
- [ ] Pull Request形式で提出すればクリア

#### 内容
HTMLファイルとCSSファイルを作成し、以下を参考にWebページを作ってみましょう。

<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90329978-57fda680-dfe4-11ea-8f30-343a4513cbeb.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90329977-5633e300-dfe4-11ea-96fe-2ebab4bbbc18.png" alt="guide.png">
</details>

#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `04_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [04/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[04/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
