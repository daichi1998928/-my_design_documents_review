# ER図2
## 全体
- 配送先テーブルを用意する
- 入荷テーブルを作り商品とのリレーションをとり入荷を管理する

## 管理者
- 他のテーブルとのリレーションの必要はない
- PKがない

## エンドユーザ
- 名の漢字用カラムがない
- 配送先は別テーブルで管理する
- テーブル名とPKを一致させる

## カートアイテム
- PKがない
- 小計金額カラムは必要ない

## 商品
- 在庫数カラムは必要ない
- deleted_atカラムを追加する
- ディスク枚数カラムは必要ない
- 発売日カラムを追加する
- ディスクテーブルとのリレーションを「1:多」にする、ディスクFKがいらない

 ## 購入
 - 姓、名カラムがない
 - 郵便番号カラムがない
 - 注文ステータスカラムがない
 - テーブル名を「受注」にする、PKもそれに合わせる
 - 購入日カラムは必要ない

 ## 購入詳細
 - 商品テーブルとダイレクトにリレーションをつける、FKが必要
 - テーブル名を「受注詳細」にする、PKもそれに合わせる
 - 購入テーブルとのリレーションが「1:多」ではなく、「多:1」にする
 - 上に伴いFKを設定する
 - 小計金額カラムは必要ない
 - 購入後価格カラムをつくる

 ## ディスク
 - トラックNoではなく、ディスクNoもしくはティスク名というようなカラムにする
 - 曲名とのリレーションを「1:多」にする、曲名FKがいらない
 - 商品IDをFKとして持たせる

 ## 曲名
 - トラックNoカラムを追加する
 - FKとしてティスクIDをつくる

 ## ジャンル
 - ジャンルでなく「ジャンル名」にする

 ## レーベル
 - レーベルではなく「レーベル名」にする

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。



# 研修担当レビュー
- 再提出の際、以下は残しておいてください。

## 全体
- カラム名から、入り得る値が推測しにくいカラムはないでしょうか。
  - 該当テーブルで指摘を加えましょう。(ジャンル、レーベルに注目しましょう！)



## 購入
- テーブル名は管理者視点である必要があります。
  - 「購入、注文」はどちらから見た命名になりますでしょうか。


## 購入詳細
- 同じく、テーブル名は管理者視点である必要があります。
