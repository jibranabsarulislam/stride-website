---
permalink: /sitemap.xml
eleventyExcludeFromCollections: true
---
<?xml version="1.0" encoding="utf-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  {% for page in collections.all %}{% unless page.url contains ".css" or page.url contains ".js" %}
  <url>
    <loc>{{ site.url }}{{ page.url | url }}</loc>
    <lastmod>{{ page.date | date: "%Y-%m-%dT%H:%M:%S%z" }}</lastmod>
  </url>
  {% endunless %}{% endfor %}
</urlset>