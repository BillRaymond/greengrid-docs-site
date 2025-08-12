---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
> This website is a fictional project created for the [AI Workshop for Content Creators](). It was designed to demonstrate documentation best practices using synthetic examples. Learn more at [BillTalksAI.com](https://www.BillTalksAI.com).

<div style="display: flex; justify-content: center; align-items: center; margin-top: 32px; margin-bottom: 32px;">
  <img src="{{ '/images/GreenGrid-logo.png' | relative_url }}" alt="GreenGrid Logo" style="max-width: 240px; width: 100%; height: auto;">
</div>

## API Docs Home
GreenGrid’s APIs help you unlock the full power of smart energy tools. Whether you’re building dashboards, syncing with smart meters, or exploring real-time usage data, our APIs provide secure, scalable access to the insights you need.

## GreenGrid API Docs

<ul>
  {% for doc in site.docs %}
    <li><a href="{{ doc | relative_url }}">{{ doc.title }}</a></li>
  {% endfor %}
</ul>
