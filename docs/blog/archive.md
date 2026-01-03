# Archive

按时间自动归档（来自 `blog/posts/`）。

{% set posts = pages | sort(attribute='meta.date', reverse=true) %}
{% for p in posts %}
- **{{ p.meta.date }}** · [{{ p.title }}]({{ p.url | url }}){% if p.meta.tags %} · {% for t in p.meta.tags %}`{{ t }}` {% endfor %}{% endif %}
{% endfor %}

---

> 提示：需要每篇文章 front matter 里包含 `date:` 字段（如 `2026-01-03`）。
