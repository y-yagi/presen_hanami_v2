#  Components

* `Providers`で登録された`Components`は、`app`配下の`Components`と同様に使用可能

```ruby
# app/publishers/send_welcome_email.rb
class SendWelcomeEmail < Bookshelf::Operation
  include Deps["email_client"]

  def call(name:, email_address:)
    result = step deliver(name:, email_address:)
  end

  private

  def deliver(name:, email_address:)
    Success(email_client.deliver(
      to: email_address,
      subject: "Welcome!",
      text_body: "<p>Welcome to Bookshelf #{name}!</p>",
      html_body:  "Welcome to Bookshelf #{name}!"
    ))
  end
end
```
