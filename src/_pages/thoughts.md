---
layout: page
title: Thoughts
paginate:
  collection: thoughts
  per_page: 5
---

<div role='thoughts-header'>Thoughts</div>
<div role='thoughts-container'>
  {% for thought in paginator.resources %}
    {% rendercontent "thought", thought: thought %}
    {% endrendercontent %}
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
  <div class="pagination">
    <span class='pagination-nav'>
      {% if paginator.previous_page %}
        <a href="{{ paginator.previous_page_path }}"><</a>
      {% else %}
        <span class='disabled-nav'><</span>
      {% endif %}
    </span>
    <span>Page {{ paginator.page }} of {{ paginator.total_pages}}</span>
    <span class='pagination-nav'>
      {% if paginator.next_page %}
        <a href="{{ paginator.next_page_path }}">></a>
      {% else %}
        <span class='disabled-nav'>></span>
      {% endif %}
    </span>
  </div>
{% endif %}
