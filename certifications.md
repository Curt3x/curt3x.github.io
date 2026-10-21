---
permalink: /certifications/
title: Certifications
lead: What I'm studying for. None of these are earned yet; I'll mark them as completed when they are.
---
<div class="grid">
{% for c in site.data.certs %}
<div class="card"><h3>{{ c.name }}</h3><div class="bar-bg"><div class="bar-fg" style="width:{{ c.progress }}%"></div></div><p class="mu">{{ c.progress }}% · {{ c.target }}</p><p>{{ c.notes }}</p></div>
{% endfor %}
</div>
