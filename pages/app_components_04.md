#  Components

* `app`ディレクトリは自動で`Components`として登録されるが、それ以外に手動で登録することも可能
* この処理を`Providers`と呼んでいる

```ruby
Hanami.app.register_provider(:email_client) do
  prepare do
    require "acme_email/client"
  end

  start do
    client = AcmeEmail::Client.new(
      api_key: target["settings"].acme_api_key,
      default_from: "no-reply@bookshelf.example.com"
    )

    register "email_client", client
  end
end
```