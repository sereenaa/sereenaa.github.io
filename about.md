---
layout: page
title: About Me
permalink: /about/

---

I am a final year student at the University of New South Wales, studying a bachelor of Data Science and Decisions. Currently a data science intern at TAL Australia, I will soon be moving into a graduate program at IAG. 

## My Website 

Navigate to my home page, and you will see a variety of blog-style posts. I'll be posting my random data science and tech projects. Come back soon to check out the updates! 

<div id="archives">
{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    
    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <h4><a href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a></h4>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>