---
layout: base
title: Category
permalink: /categories/
---
<h1>Categories</h1>
This is where you could find articles for various categories:
<ul>
    {% for category in site.categories %}
    <li><a href="{{ category.url }}">{{ category.name }}</a></li>
{% endfor %}
</ul>

```sql
select * from users;
```

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```