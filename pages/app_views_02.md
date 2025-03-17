#  Templates

```ruby
# app/templates/books/index.html.erb
<h1>Books</h1>

<ul>
  <% books.each do |book| %>
    <li><%= book[:title] %>, by <%= book[:author] %></li>
  <% end %>
<h1>Books</h1>
```