#  Relations

* データを取得する為のメソッドを定義することも出来る
* `Relations`に定義するメソッドはchainableである必要がある
  * romの`Relation`クラスを返す必要がある
* 例えば、`Relation#to_a`は実際にDBからデータを取得するので使用出来ない