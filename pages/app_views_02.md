#  Views

* `expose`でテンプレートで使用するデータの設定を行う

```ruby
# app/views/books/index.rb
module Bookshelf
  module Views
    module Books
      class Index < Bookshelf::View
        include Deps["repos.book_repo"]

        expose :books do |page:, per_page:|
          book_repo.all_by_title(page:, per_page:)
        end
      end
    end
  end
end
```

* 謎の`Deps`については後で説明します