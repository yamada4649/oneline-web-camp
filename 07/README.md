# 7章【メイン部分を作ろう】

## 課題概要
 - 継続課題 : 1問
 - 確認問題 : 4問
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
   1. `continuous_exercise_07`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_07`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_07`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_07`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_07`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
#### 問１
行の高さを30pxに設定したい場合は、どのプロパティと値を指定しますか。次から選んでください。
- a. line-height: 30;
- b. line-height: 30px;
- c. row-height: 30;
- d. row-height: 30px;

<details>
<summary>解答はこちら</summary>

#### 解答
【b】

#### 解説
**行の高さを設定する**<br>
行の高さを設定するプロパティはline-heightプロパティです。<br>
また、その値は単位を持つか持たないかによって意味が変わってくるのはコンテンツの通りなので、確認してください。
</details>

#### 問２
HTMLにてsectionタグを設定し、CSSで幅300px、高さ300px、太さが2px、種類が直線、色が#fa5893の枠線を指定してください。

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
    <!-- CSSファイルの読み込み -->
    <link rel="stylesheet" href="style.css" />
    <title>7章 確認問題</title>
  </head>
  <body>
    <section></section>
  </body>
</html>
```

【style.css】
```css
section {
  width: 300px;
  height: 300px;
  border: 2px solid #fa5893;
}
```
</details>

#### 問３
問２で作成したsection要素内に見出しタグを設定し、タグ内に「折り返し地点」の文字を入力してください。

#### 問４
spanタグを用いて、「折り返し地点」の「地点」のみ、文字色を#fa5893に変更してください。

<details>
<summary>問３・４の解答はこちら</summary>

#### 解答
HTML/CSSはこちら<br>
【index.html】
```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <!-- CSSファイルの読み込み -->
    <link rel="stylesheet" href="style.css" />
    <title>7章 確認問題</title>
  </head>
  <body>
    <section>
      <h1>折り返し<span>地点</span></h1>
    </section>
  </body>
</html>
```

【style.css】
```css
span {
  color: #fa5893;
}
```
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
<img src="https://user-images.githubusercontent.com/57278701/90330055-e5d99180-dfe4-11ea-96a9-5731d21bef64.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90330057-e83beb80-dfe4-11ea-8926-fa9357c74265.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `07_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [07/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
      1. 課題に取り組む際に必要な画像ファイルは、既にディレクトリ[07/exercise_01/img](./exercise_01/img)に配置してあります。
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[07/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
