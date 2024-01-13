---
layout: page
title: Thoughts
---

<div role='thoughts-header'>{{ data.title }}</div>
<div role='thoughts-container'>
  {% for thought in collections.thoughts.resources reversed %}
    {% rendercontent "thought", thought: thought %}
    {% endrendercontent %}
  {% endfor %}
</div>
