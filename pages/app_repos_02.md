#  Repos

* `Repos`からは`Relations`を直接参照出来るようになっている
  * 先のexampleにおける`books`
* `Relations`にデータストアを意識した処理を定義する事で、`Repos`はデータストアを意識せずCRUDを行えるように出来る、ようにするのを目指していると感じた
  * romのドキュメントだとそもそも`Relations`にメソッドを定義するのを推奨してないように見えるが…
* `Actions`などからDBに関する処理を行う場合、直接`Relations`を操作するのではなく、`Repos`を使用するのが推奨されている
