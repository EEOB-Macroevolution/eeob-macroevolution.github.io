---
title: Help file in category help
icon: fa-comment
categories: [help,work]
category: categories help
order: 2
---
This file is categorized in the Front Matter.

```
title: {{ page.title }}
layout: {{ page.layout }}
categories: [{{ page.categories | join: ","}}]
icon: {{ page.icon }}
order: {{ page.order }}
```

So it belongs to categories assistanche, help, work in the others collection.
