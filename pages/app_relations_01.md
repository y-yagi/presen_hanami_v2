#  Relations

* DBのテーブルとの関連付けを行う
* `schema`メソッドに`infer`オプションをつけると、テーブルの情報からattributesを設定してくれる
* associationsの指定もここ

```ruby
# app/relations/books.rb
module Bookshelf
  module Relations
    class Books < Bookshelf::DB::Relation
      schema :books, infer: true
        associations do
          belongs_to :publisher
        end
      end
    end
  end
end
```
