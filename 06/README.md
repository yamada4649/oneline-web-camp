# 6章【メインビジュアルを作ろう】

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
   1. `continuous_exercise_06`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_06`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_06`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行いましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_06`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_06`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。


---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問１
背景画像を設定するプロパティは、次のうちどれでしょう。
- a. background-position
- b. background-size
- c. background-image
- d. background-color

<details>
<summary>解答はこちら</summary>

#### 解答
【c】

#### 解説
**背景の設定**<br>
background-imageは、HTMLで生成した箱に背景画像を設定するためのプロパティです。<br>
値に url() というものが必要になるので注意してください。()内に画像までのパスを書きます。
</details>

### 問２
色を指定する方法は、代表的なものとして3種類あります。すべての指定方法で「赤」を指定してください。

<details>
<summary>解答はこちら</summary>

#### 解答
【CSSファイル】
```css
セレクタ {
  color: red;
  color: #ff0000;  /* color: #f00; でも同じ意味です。*/
  color: rgb(255, 0, 0);
}
```

#### 解説
**色指定の方法**<br>
色を指定する方法は次の3種類あります。<br>
１. 色名<br>
red, green, yellowなど、メジャーな色であればその名称で指定できます。<br>
２. 16進数のカラーコード<br>
#aabbcc のように、16進数で指定された6桁の数字で色が決められます。<br>
最初の2桁がrgbのr、次の2桁がg、最後の2桁がbです。<br>
３. rgbそれぞれの値を設定する<br>
rgbの各要素に対応する0～255までの数字を指定します。
</details>

### 問３
次のpタグに囲まれた文字の書き方で、正しいのはどちらでしょう。
- a.
【HTMLファイル】
```html
<p>私の名前はWebCampです。これから</p>
<p>一緒にスキルをより磨きましょう！</p>
```
- b.
【HTMLファイル】
```html
<p>
  私の名前はWebCampです。これから<br />
  一緒にスキルをより磨きましょう！
</p>
```

<details>
<summary>解答はこちら</summary>

#### 解答
【b】

#### 解説
**段落の使い方(インデント)**<br>
pタグはparagraph（段落）の頭文字を指します。<br>
そのため、一つのまとまった意味を持つ文章に改行を入れるという目的で複数のp要素を入れることはいいことではありません。<br>
まとまった文章で改行を入れたい場合はbrタグを使いましょう。
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
<img src="https://user-images.githubusercontent.com/57278701/90330041-c5a9d280-dfe4-11ea-86ef-b341470d7a27.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/57278701/90330042-c8a4c300-dfe4-11ea-9c8a-e6f61225615d.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBranchを作成します。
   1. ブランチ名は `06_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [06/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
      1. 課題に取り組む際に必要な画像ファイルは、既にディレクトリ[06/exercise_01/img](./exercise_01/img)に配置してあります。
   1. ダウンロードしたimg.zipは解答し、imgディレクトリも[06/exercise_01](./exercise_01)直下に配置して下さい。
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[06/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
