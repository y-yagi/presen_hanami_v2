#  Operations

```bash
$ bundle exec hanami generate operation books.create
```

↑のコマンドで下記ファイルが生成される

```ruby
# app/books/create.rb
module Bookshelf
  module Books
    class Create < Bookshelf::Operation
      def call
      end
    end
  end
end
```

* 上記例だと`app`配下に`books`が作成される
  * `operations.books.create`のように、ネストを深くする事も可能
* dry-rbのライブラリの1つである[dry\-operation](https://dry-rb.org/gems/dry-operation/)をそのまま使用している
