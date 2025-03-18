#  Repos

* データのロードや作成など、DBの操作に関する処理を定義する場所

```ruby
# app/repos/book_repo.rb
module Bookshelf
  module Repos
    class BookRepo < Bookshelf::DB::Repo
      def get(id)
        books.by_pk(id).one!
      end

      def create(attributes)
        books.changeset(:create, attributes).commit
      end

      def latest(page: 1)
        books.order_by_latest.page(page).to_a
      end
    end
  end
end
```