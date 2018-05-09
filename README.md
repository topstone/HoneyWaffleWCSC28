# HoneyWaffleWCSC28

（アップロード作業中）

## エンジン、定跡ファイル、評価関数のセット

https://drive.google.com/file/d/1eczNX5zMiAKwmBg-IMj25Fq2vFYBE0lJ/view?usp=sharing

エンジンと定跡ファイル（user_book2.db）、評価関数のセットです。
AVX2対応版とSSE42版を同梱しています。

### エンジンの登録

HoneyWaffle_WCSC28_AVX2.exeを選択して登録してください。何かエラーが発生した場合は、HoneyWaffle_WCSC28_sse42.exeを試してみてください。
なおどちらもエラーとなる場合、お使いのPCでは起動ができないと思われます。

### エンジンの設定（例）

このあたりは通常のやねうら王と同じように設定してください。

![エンジンの設定](https://github.com/32hiko/HoneyWaffleWCSC28/blob/master/engine_ss_2018-05-10%2000.20.02.png)

### 定跡ファイルの設定

以下のようにuser_book2.dbを選択し、BookMovesは80、その他のBookなんとかは全部0にしてください。

![定跡ファイルの設定](https://github.com/32hiko/HoneyWaffleWCSC28/blob/master/book_ss_2018-05-10%2000.05.00.png)


以下、ライブラリからの改変について

（エンジンそのものの改変部分を追記する）

（評価関数の説明を追記する）

## 定跡ファイル（やねうら王形式）

https://github.com/32hiko/HoneyWaffleWCSC28/blob/master/user_book2.db

SDT5版の定跡をベースにしました。当然、振り飛車定跡です。

やねうら王にApery評価関数を搭載したものを相手に、定跡なし or 「まふ定跡横歩取り(SDT5で平成将棋合戦ぽんぽこさんが公開したもの)」をのせ、1手60秒6スレッド、投了値500で対戦。（これはうちの環境で2億ノード程度になります。）  
80手までの手順のうち、振り飛車が有利または互角の部分だけを目検で吟味して採用しています。  
※私がアマチュア級位者レベルなのに、そういうことをやっているので、変な手順が混入している可能性は大いにあります。  
間違えて居飛車にならないよう、居飛車側の手は含んでいません。純粋に対局目的の定跡で、人間が読むことは想定していません。  
