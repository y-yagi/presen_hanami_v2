#  Operations

* じゃあビジネスロジックをどこで実装するかというと、別途`Operations`という、ビジネスロジックを実装するための機能がある
  * 俗にいう「サービスレイヤー」

```bash
$ bundle exec hanami generate operation books.create
```

```ruby
module Bookshelf
  module Books
    class Create < Bookshelf::Operation
      def call
      end
    end
  end
end
```

* dry-rbのライブラリの1つである[dry\-operation](https://dry-rb.org/gems/dry-operation/1.0/)をそのまま使用している