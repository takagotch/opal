### opal

https://github.com/opal/opal

```
opal --copile app.rb > app.js



```

```ruby
# app.rb
puts 'Hello!'

Opal.compile("puts 'wow'") # => "(function() { ... self.$put("wow"); ...})"





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






```


