#  Structs

* `Structs`を拡張したい場合、`Struct` classを継承したクラスを作成すればOK

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
