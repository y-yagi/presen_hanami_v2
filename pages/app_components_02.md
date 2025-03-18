#  Components

```ruby
class Show < Bookshelf::View
  include Deps["repos.book_repo"]

  expose :book do |id:|
    book_repo.get(id)
  end
end
```

上記は下記のコードと同一

```ruby
class Show < Bookshelf::View
  expose :book do |id:|
    Bookshelf::Repos::BookRepo.new.get(id)
  end
end
```