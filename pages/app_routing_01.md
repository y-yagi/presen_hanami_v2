#  Routing

* 概ね見ての通り

```ruby
# config/routes.rb
module Bookshelf
  class Routes < Hanami::Routes
    root to: "home.index"
    get "/books", to: "books.index"
    get "/books/:id", to: "books.show", as: :show_book
    get "/books/new", to: "books.new"
    post "/books", to: "books.create", as: :create_book
    post "/publishers", to: "publishers.create", as: :create_publisher
    get "/publishers/new", to: "publishers.new"
    get "/publishers/:id", to: "publishers.show", as: :show_publisher
  end
end
```