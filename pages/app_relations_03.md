#  Relations

```ruby
# app/relations/books.rb
module Bookshelf
  module Relations
    class Books < Bookshelf::DB::Relation
      # これはOK
      def order_by_latest
        order(self[:id].desc)
      end

      # これはNG
      def order_by_latest
        order(self[:id].desc).to_a
      end
    end
  end
end
```