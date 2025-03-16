#  Structure

* アプリケーションのコードは基本`app`配下に格納する。アプリ生成時点での`app`配下は下記の通り。
  * 本当は`assets`ディレクトリもあるのですが省略しています

```bash
├── action.rb
├── actions
├── db
│   ├── relation.rb
│   ├── repo.rb
│   └── struct.rb
├── operation.rb
├── relations
├── repos
├── structs
├── templates
│   └── layouts
│       └── app.html.erb
├── view.rb
└── views
    └── helpers.rb
```
