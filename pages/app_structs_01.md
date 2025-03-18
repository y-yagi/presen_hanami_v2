#  Structs

* 先に記載した通り、`Repos`は`Structs`を返す
* `Structs`を拡張したい場合、独自の`Struct`を継承したクラスを作成すれば良い

```ruby
# app/structs/book.rb
module Bookshelf
  module Structs
    class Book < Bookshelf::DB::Struct
      TAX = BigDecimal("1.10")

      def price_with_tax
        (price * TAX).to_i
      end
    end
  end
end
```

```ruby
Bookshelf::Repos::BookRepo.new.latest.first.price_with_tax
```