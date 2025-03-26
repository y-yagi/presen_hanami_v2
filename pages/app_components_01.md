# Components

* ここからは、後回しにした`Deps`について

```ruby
# app/views/books/index.rb
module Bookshelf
  module Views
    module Books
      class Index < Bookshelf::View
        include Deps["repos.book_repo"]  # ← これ

        expose :books do |page:, per_page:|
          book_repo.all_by_title(page:, per_page:)
        end
      end
    end
  end
end
```
