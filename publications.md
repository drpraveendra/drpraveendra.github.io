{% for pub in site.data.publications %}
{{ pub.title }}  
{{ pub.author }}  
{{ pub.journal }} ({{ pub.year }})

{% endfor %}
