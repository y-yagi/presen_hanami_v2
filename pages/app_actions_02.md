#  Actions

* `Actions`でvalidationを行う

```ruby
# app/actions/books/create.rb
module Bookshelf
  module Actions
    module Books
      class Create < Bookshelf::Action
        params do
          required(:book).hash do
            required(:publisher_id).filled(:integer)
            required(:title).filled(:string)
            required(:author).filled(:string)
            required(:price).filled(:integer, gteq?: 0)
          end
        end

        def handle(request, response)
          # ...
        end
      end
    end
  end
end
```
