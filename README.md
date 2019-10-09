# Mirai_Proofreading

## 概要

記事をリアルタイム、かつ自動で校正してくれます。  
使い方、挙動の詳しい情報は以下の動画をご覧ください。  
https://www.youtube.com/watch?v=M8xn9wpwJkQ

## 機能

### prh.ymlファイル

**prh.yml**ファイルに単語を指定することで、入れ替えたい単語をいくつでも登録できます。

```txt:prh.yml

version: 1
rules:
  - pattern: お勧め
    expected: おすすめ
```

``pattern:``の次に誤った表記、``expected:``の次に正しい表記を登録します。  
上の例の場合、記事に``お勧め``と入力すると、``おすすめ``にしろというエラーが表示されます。
  
  
  
### .textlintファイル

プラグインをインストールすることで、校正の基準を設けることが可能です。  
falseになっている項目は、機能をoffにしています。  
以下に、標準でインストールされている機能を紹介します。  
  
https://github.com/textlint-ja/textlint-rule-preset-japanese  
一般的な文書で利用するためのルール集です。  
  
https://github.com/textlint-ja/textlint-rule-no-doubled-joshi  
文中に同じ助詞が複数出てくるのをチェックします。  
  
https://github.com/textlint-ja/textlint-rule-preset-ja-technical-writing  
技術文書向けのルール集です。
  
https://github.com/textlint-ja/textlint-rule-no-mixed-zenkaku-and-hankaku-alphabet  
全角と半角アルファベットを混在をチェックします。  
  
https://github.com/textlint-ja/textlint-rule-preset-JTF-style  
JTF日本語標準スタイルガイドです。
  
https://github.com/textlint-ja/textlint-rule-prefer-tari-tari  
例示・並列・対表現の「〜たり〜たりする」をチェックします。  
**現在うまく動作しません。**
