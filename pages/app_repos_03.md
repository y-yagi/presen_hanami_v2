#  Repos

* `to_a`や`one`を使用してデータがデータストアからロードされた場合、`Structs`のインスタンスが返ってくる

```ruby
Bookshelf::Repos::BookRepo.new.latest.class # => Bookshelf::Structs::BookのArray
Bookshelf::Repos::BookRepo.new.get(1).class #=> Bookshelf::Structs::Book
```

* `Structs`はDBのコネクションを持たないので、`Structs`になった後にDBへのロードが発生する事は無い
  * そのため、N+1は発生しない(出来ない)