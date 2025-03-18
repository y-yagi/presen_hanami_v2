#  Components

* `app`ディレクトリ配下にある`Components`のキーは、ディレクトリ名+ファイル名で生成される
  * `app/repos/book_repo.rb`にある場合、キーは`repos.book_repo`になる
* はアプリケーションの`container`は`Hanami.app`で参照出来、ここから直接`Components`の取得も出来る
* 例えば、テストで、`Hanami.app["relations.books"]`とすると、簡単に`Relations`の取得が出来る