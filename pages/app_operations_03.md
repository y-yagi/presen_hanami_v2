#  Operations

* パブリックメソッドは`call`だけ
* `step`の戻り値は必ず`Success`か`Failure`である必要がある
  * この`Success`と`Failure`は[dry\-monads](https://dry-rb.org/gems/dry-monads/)のクラス
* `step`の戻り値が違うクラスの場合、`dry-operation`がエラーを返す