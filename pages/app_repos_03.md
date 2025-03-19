#  Repos

* `Repos`は`Structs`を返す

```ruby
Bookshelf::Repos::BookRepo.new.latest.class # => Array
Bookshelf::Repos::BookRepo.new.latest.first.class # => Bookshelf::Structs::Book
```

* `Structs`はDBのコネクションを持たないので、`Structs`になった後にDBへのロードが発生する事は無い
