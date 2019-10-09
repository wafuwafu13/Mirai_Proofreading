# Mirai_Proofreading

## 概要

記事をリアルタイム、かつ自動で校正してくれます。  
使い方、挙動の詳しい情報は以下の動画をご覧ください。  
https://www.youtube.com/watch?v=M8xn9wpwJkQ  
**後で変える**

## 機能

### prh.ymlファイル

**prh.yml**ファイルに単語を指定することで、入れ替えたい単語をいくつでも登録できます。

```txt:prh.yml

version: 1
rules:
  - pattern: お勧め
    expected: おすすめ
```

``pattern:``の次に**誤った表記**、``expected:``の次に**正しい表記**を登録します。  
上の例の場合、記事に``お勧め``と入力すると、``おすすめ``にしろというエラーが表示されます。
  
  
  
### .textlintrcファイル

プラグインをインストールすることで、校正の基準を設けることが可能です。  
**false**になっている項目は、機能をoffにしています。  
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
  
https://github.com/io-monad/textlint-rule-general-novel-style-ja  
日本の小説における一般的な作法に従うためのルール集です。  
  
https://github.com/lostandfound/textlint-rule-ja-hiragana-keishikimeishi  
漢字よりもひらがなで表記したほうが読みやすい形式名詞を指摘します。  
  
https://github.com/lostandfound/textlint-rule-ja-hiragana-fukushi  
漢字よりもひらがなで表記したほうが読みやすい副詞を指摘します。  
  
https://github.com/lostandfound/textlint-rule-ja-hiragana-hojodoushi  
漢字よりもひらがなで表記したほうが読みやすい補助動詞を指摘します。  
  
https://github.com/textlint-ja/textlint-rule-no-insert-dropping-sa  
サ抜き、サ入れ表現の誤用をチェックします。
