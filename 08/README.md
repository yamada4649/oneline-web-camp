# 8章【サイドバーを作ろう】

## 課題概要
 - 継続課題 : 1問
 - 確認問題 : 2問
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
   1. `continuous_exercise_08`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_08`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_08`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行いましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_08`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_08`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。

### 問１
CSSにて、以下のようにidセレクタで「文字色を赤に設定」の場合と、classセレクタで「文字色を青に設定」の場合とでは、<br>
どちらの設定が反映されるでしょうか。<br>
【HTMLファイル】
```html
<p id="red" class="blue">この文字の色は何色になるでしょう</p>
```

【CSSファイル】
```css
#red {
  color: red;
}
.blue {
  color: blue;
}
```

<details>
<summary>解答はこちら</summary>

#### 解答
【id名をセレクタに設定したスタイルが適用される】

#### 解説
**詳細度**<br>
CSSには詳細度という概念があります。詳細度とは、スタイルの指定が重複したときにどのスタイルを優先するかという優先度を定量評価したものです。<br>
詳細度の強さは次のように決められています。詳しくは更に多くありますが、ここでは有名なところを提示します。<br>
（）は具体的な例です。
1. Inline style … （`<p style=""></p>`）
2. IDセレクタ … （`#red`）
3. 疑似クラス … （`nth-child(n)`、`:hover`）
4. クラスセレクタ … （`.blue`）
5. タイプセレクタ … （`p{...}`、`h1{...}`）
6. 全称セレクタ … （`*{...}`）

詳細度はWebページ内で一定に保つことが適切とされています。<br>
そのため、一番使いやすいクラスセレクタを使うことが一般的です。<br>
これまでに執拗にclass名を付けてくださいと伝えてきたのはこのような理由があります。
</details>

### 問２
疑似クラスを書く際に使う記号として正しいものは、次のうちどれでしょう。
- a. p/nth-child(n)
- b. p;nth-child(n)
- c. p%nth-child(n)
- d. p:nth-child(n)

<details>
<summary>解答はこちら</summary>

#### 解答
【d】

#### 解説
**疑似クラス**<br>
疑似クラスは使い勝手がよく、HTMLにクラス名を追加などしなくてもスタイルを定義できるので、しっかりと確認しましょう。
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
<img src="https://user-images.githubusercontent.com/57278701/90330109-51236380-dfe5-11ea-80e0-7d806f2f0e51.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90330111-541e5400-dfe5-11ea-9d2d-83df1ffa4a0a.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `08_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [08/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[08/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
