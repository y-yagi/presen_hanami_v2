#  Components

* `app`ディレクトリ配下のファイルは、それぞれ単一の責務を持つ`Components`として扱われる
  * 例えば、`BookRepo`クラスは、`books`テーブルの操作に対する責務を持つ`Components`
* Hanamiはこの`Components`を、アプリケーションという`Container`に追加し、アプリで簡単に使用出来るようにしている
* `include Deps`はこの`Components`使うようにする為の処理
