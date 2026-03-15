---
layout: default
title: "📝 Mathematics Blog"
permalink: /blog/
---

# 📝 Mathematics Blog

Concepts, theorems, and solved problems explained clearly — for B.Sc., M.Sc., CSIR NET, GATE, and IIT JAM students.

---

{% for post in site.posts %}
### [{{ post.title }}]({{ post.url }})
*{{ post.date | date: "%B %d, %Y" }}*

{{ post.description }}

[Read More →]({{ post.url }})

---
{% endfor %}

{% if site.posts.size == 0 %}
*New posts coming soon. Stay tuned!*
{% endif %}
```

---

**5. `robots.txt`** — Create this new file in the root:
```
User-agent: *
Allow: /

Sitemap: https://drpraveendra.github.io/sitemap.xml
