# vue-sample-todo
WEB+DB PRESS Vol.120のVue特集のsampleアプリを作成

このコードでは１〜３章の内容を写経しています

#### 第2章の内容は以下です
## TODOリストの要件
- TODOをリストする機能
- TODOを追加する機能
- TODOを完了にする機能
- TODOをフィルタする機能

## 学習内容
- dataオプション
- v-bindオプション
- v-forディレクティブ
- v-modelディレクティブ
  - 双方向ディレクティブ
- v-on
  - イベントハンドラの登録
- methodsオプション
  - 登録したメソッドをコンポーネントのメソッドとして活用できる
- v-if
  - 条件による表示の切り替え
  - 同じようなものに`v-show`がある

### v-if

- falseの場合に要素を描画しない
    - 初期描画コストが低い
    - 切り替えコストが高い

### v-show

- falseの場合でも要素を描画した上でスタイルによって非表示にしている(display: none)
    - 初期描画コストが高い
    - 切り替えコストは低い

[vue.jsのcomputedとmethodsの使い分け](https://zenn.dev/naoki_oshiumi/articles/8c99581ca5bdd0)
[猿でも分かる！Vueのリアクティブシステム](https://zenn.dev/kj455/articles/c740c72edeabbe)

## 第3章
- プロパティ
- カスタムイベント
- スロット
- provide/inject