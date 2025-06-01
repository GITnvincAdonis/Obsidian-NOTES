---
creation date: <% tp.file.creation_date() %>
---
Set up:

> [!NOTE] [[https://github.com/simplecov-ruby/simplecov|Documentation]]
> 

1. Add to gem file under test block
   
```
  gem 'simplecov', require: false
```


2. Add to spec helper file
   
```
require 'simplecov'
SimpleCov.start 'rails'

# Previous content of test helper now starts here
```

3. Run all tests. In the case of an Rspec suite, use 'rspec' in the terminal

4. Open coverage Html in desired browser (use command in a terminal of same project)

```
firefox  coverage/index.html  
```

Link to original: [[2025-04-02]]