#  Migrations

* romのmigration APIを使用している
* Railsと異なり、ファイルの格納先は`config/db`配下

```ruby
# config/db/migrate/20250309111940_create_books.rb
ROM::SQL.migration do
  # See https://guides.hanamirb.org/v2.2/database/migrations/ for details.
  change do
    create_table :books do
      primary_key :id
      column :title, :text, null: false
      column :author, :text, null: false
    end
  end
end
```
