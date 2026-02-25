---
layout: default
---

## Latest Updates

Welcome to my blog! Below you will find a chronological list of my recent posts.

<ul>
  {% for post in site.posts %}
    <li style="margin-bottom: 20px; list-style: none;">
      <!-- 标题 -->
      <h3 style="margin-bottom: 5px;">
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <!-- 日期 -->
      <div style="color: #666; font-size: 0.9em;">发布于 {{ post.date | date: "%Y-%m-%d" }}</div>
      <!-- 预览内容 (自动截取第一段) -->
      <div style="margin-top: 10px; color: #333;">
        {{ post.excerpt | strip_html | truncatewords: 50 }}
      </div>
      <a href="{{ post.url | relative_url }}" style="font-size: 0.9em;">阅读全文 →</a>
    </li>
  {% endfor %}
</ul>
