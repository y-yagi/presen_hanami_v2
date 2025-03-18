#  Repos

* `Repos`からは`Relations`を直接参照出来るようになっている
  * 先のexampleにおける`books`
* `Actions`などからDBに関する処理を行う場合、直接`Relations`を操作するのではなく、`Repos`を使用するのが推奨されている
* `Repos`は`Structs`を返す

```ruby
Bookshelf::Repos::BookRepo.new.latest.class # => Array
Bookshelf::Repos::BookRepo.new.latest.first.class # => Bookshelf::Structs::Book
```

* `Structs`はDBのコネクションを持たないので、`Structs`になった後にDBへのロードが発生する事は無い