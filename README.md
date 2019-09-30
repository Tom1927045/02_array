# 配列

# 進め方
## はじめてのとき
* [GitHub](https://github.com/)のアカウントを作成してください
* [Travis CI](https://travis-ci.com/) のアカウントを作成してください
* GitHubのアカウントを[こちらのフォーム](https://forms.gle/k5zoXyy4yAWNPz4KA)から教えてください。
## 毎回の進め方
* このリポジトリをforkしてください
* Travis CI を設定して、自動ビルドが通るようにしてください
   * Travis CI のGitHubアカウントでの登録とforkしたリポジトリをTravisCI側で許可する
   * 参考サイト：[Travis CIで自動テストして、結果をGitHubのトップページに表示する](https://qiita.com/hoshimado/items/4090d8e64beb8a7f95e1)
* forkしたリポジトリの README.md ファイルの「t-kougei-game-comp-2019」の部分を自分のGitHubアカウント名に差し替えてください(2箇所)
* 問題を解いて、テストを通るようにしてください。
* fork 元の master ブランチにプルリクエストを投げてください

# テスト結果

[![Build Status](https://travis-ci.com/Tom1927045/02_array.svg?branch=master)](https://travis-ci.com/t-kougei-game-comp-2019/02_array)

# 今回の問題

配列の勉強です。

入力される文字を配列に順次格納して、取り出すように指示されたら、その値を出力してください。

input?.txt ファイルを標準入力として読み込んで、標準出力の結果を output?.txt ファイルと一致するか比較するテストをします。

main.c ファイルだけを書き換えて下さい。

## 入力される値
入力は以下のフォーマットで与えられます。
~~~
n
n
n
n
~~~
* n: 値が0か正なら、配列に順番に格納する。負の値なら、配列の(-n)番目の要素を出力する

## 期待する出力

入力されたデータの内、負の値の行数の数だけ数字を出力します。

最後は改行し、余計な文字、空行を含んではいけません。

## 条件
すべてのテストケースで以下の条件を満たします。
* 入力される値は全て整数
  * -100 ≦ n ≦ 100
* テストデータの行数は100行を超えることはありません

## 入力例1
~~~
3
-1
~~~
* 1行目の数字は正なので、配列に格納することを期待します（例えば、array[0]=3;）
* 2行目の数字は負なので、配列に格納された値から入力の絶対値である「1」番目の要素の値(3)を出力することを期待します。

## 出力例1
~~~
3
~~~

## 入力例2
~~~
5
7
0
-2
4
-4
~~~

## 出力例2
~~~
7
4
~~~
