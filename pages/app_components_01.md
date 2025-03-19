#  Components

* `app`ディレクトリ配下のファイルは、それぞれ単一の責務を持つ`Components`として扱われる
  * 例えば、`BookRepo`クラスは、`books`テーブルの操作に対する責務を持つ`Components`
* Hanamiはこの`Components`をアプリケーションという`Container`に追加し、簡単に使用出来るようにしている
* `include Deps`はこの`components`使うようにする為の処理