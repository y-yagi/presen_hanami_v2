#  Operations

* 呼び出す側

```ruby
# app/actions/publishers/create.rb
def handle(request, response)
  case create.call(request.params[:publisher])
  in Success(publisher)
    response.flash[:notice] = "publisher created"
    response.redirect_to routes.path(:show_publisher, id: publisher.id)
  in Failure[:invalid, validation]
    response.flash.now[:alert] = "Could not create publisher: #{validation}"
  end
end
```

* `Success`と`Failure`は実際の値をラップしたクラスなので、実際の値がどうなるかについては特に制限は無し