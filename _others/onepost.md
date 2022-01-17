---
title: Help file in category help
layout: post
categories: [help,assistance]
date: 24/4/2018
icon: fa-comment
order: 2
---

You can even create posts in collections and assign categories to them.
You simply have to declare the layout and a date of publishing, if your  file name does not follow the jekyll naming convention for posts.
```
title: {{ page.title }}
layout: {{ page.layout }}
categories: [{{ page.categories | join: ","}}]
date: {{ page.date |date: "%d/%m/%Y"}}
icon: {{ page.icon }}
order: {{ page.order }}
```
