#  Actions

* HTTPリクエストの処理をするための機能
  * Railsにおけるcontroller
* Railsにおけるcontrollerのaction毎にクラスを作成する

```ruby
# app/actions/books/new.rb
module Bookshelf
  module Actions
    module Books
      class New < Bookshelf::Action
        def handle(request, response)
        end
      end
    end
  end
end
```

* `response`に`response.body = "Welcome to Bookshelf"`のように直接レスポンスの設定もできる