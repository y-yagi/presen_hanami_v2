#  Components

* `app`ディレクトリ配下にある`Components`のキーは、ディレクトリ名+ファイル名で生成される
  * `app/repos/book_repo.rb`にある場合、キーは`repos.book_repo`になる
* アプリケーションの`Container`は`Hanami.app`で参照出来るようになっており、ここから直接`Components`の取得も出来る
* 例えば、テストで、`Hanami.app["relations.books"]`とすると、`Bookshelf::Relations::Books`のインスタンスが取得出来る
