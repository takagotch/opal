### opal

https://github.com/opal/opal

```
opal --copile app.rb > app.js

git submodule update --init
bundle install
npm install -g jshint
bundle exec rake
rake mspec
rake rspec

```

```ruby
# app.rb
puts 'Hello!'

Opal.compile("puts 'wow'") # => "(function() { ... self.$put("wow"); ...})"

Opal::Builder.build('opal') # => "(function() { ... })()"

builder = Opal::Builder.new
builder.build_str('require "opal"; puts "wow"', '(inline)')
File.write 'app.js', builder.to_s

```

```html
<script src="app.js"></script>

<!DOCTYPE>
<html>
  <head>
    <meta charset="utf-8">
    <script src="app.js"></script>
  </head>
</html>


<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <script src="https://cdn.opalrb.com/opal/current/opal.js" onload="Opal.load('opal')"></script>
    <script src="https://cdn.opalrb.com/opal/current/opal-parser.js" onload="Opal.load('opal-parser')"></script>
    <script type="text/ruby">
      puts "hi"
    </script>
  </head>
  <body>
  </body>
</html>

```


