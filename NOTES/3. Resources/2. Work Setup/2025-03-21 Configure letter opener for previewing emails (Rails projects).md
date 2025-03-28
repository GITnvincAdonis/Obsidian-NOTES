---
creation date: <% tp.file.creation_date() %>
---

> [!NOTE] What is Letter_opener
> 

Letter opener is an email previewing gem. When a mailer class is triggered, the associated mailer views are displayed directly in the browser.


> [!Danger] Setup
> 

1. add gem to Rails gemfile:
```
gem "letter_opener", group: :development
```

This assumes that a development block doesn't exist. Ensure that if one does only the gem is added.

2. Then set the delivery method in config/environments/development.rb
```
config.action_mailer.delivery_method = :letter_opener
config.action_mailer.perform_deliveries = true
```

3. Install gem 
```
bundle
```

Link to original: [[2025-03-21]]