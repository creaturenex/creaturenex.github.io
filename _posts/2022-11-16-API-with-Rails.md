---
layout: post
title:  "API's with Rails"
date:   2022-11-16
categories: rails api
---
I was trying to build an API from memory and I couldn't remember how to do namespacing.
I found this older article [building-awesome-rails-apis](https://collectiveidea.com/blog/archives/2013/06/13/building-awesome-rails-apis-part-1) The main takeaways are these.
```ruby
namespace :api do
  namespace :v1 do
    resources :people
      # can also do nested resources
  end
end
```
I did remember to create a new directory in controllers `app/controllers/api/v1`
and created a new copy of the controller in the new directory but I forgot to
update the classname.

**before:**
```ruby
class CharactersController < ApplicationController
  ...
end
```

**after:**
```ruby
class API::V1::CharactersController < ApplicationController
  ...
end
```

Also I also learned about Rails inflections so by adding the following in `config/initializers/inflections.rb`

```ruby
ActiveSupport::Inflector.inflections(:en) do |inflect|
  inflect.acronym 'API'
end
```

I can use `API::V1` rather than `Api::V1`

**NOTES**

The article mentioned to serve your api in a subdomain, but I did not do that in
this example. I need to read more into that subject.

In addition, the article also mentions to serve JSON, but I am unsure if this is because the orginal example is full rails app and my test app is an rails API only app.

**example given:**
```ruby
def index
  @people = Person.all
  respond_to do |format|
    format.json { render :json => @people }
  end
end
```
**my app**
```ruby
def index
  @characters = Character.all

  render json: @characters
end
```
