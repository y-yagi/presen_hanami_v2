#  Operations

* ビジネスロジックをどこで実装するかというと、別途`Operations`という、ビジネスロジックを実装するための機能がある
  * 俗にいう「サービスレイヤー」

```bash
$ bundle exec hanami generate operation books.create
```

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

* 上の例だと`app`配下に`books`が作成される
* dry-rbのライブラリの1つである[dry\-operation](https://dry-rb.org/gems/dry-operation/)をそのまま使用している
