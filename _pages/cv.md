---
permalink: /cv/
title: "CV"
author_profile: true
---

{% include base_path %}

# {{ site.data.cv.basics.name }}

{{ site.data.cv.basics.summary }}

- **Email:** [{{ site.data.cv.basics.email }}](mailto:{{ site.data.cv.basics.email }})
- **Website:** [{{ site.data.cv.basics.website }}]({{ site.data.cv.basics.website }})
- **Location:** {{ site.data.cv.basics.location.address }}

## Education
{% if site.data.cv.education and site.data.cv.education.size > 0 %}
{% for edu in site.data.cv.education %}
### {{ edu.institution }} — {{ edu.area }}
{{ edu.startDate }} — {{ edu.endDate }}
{% if edu.gpa %}GPA: {{ edu.gpa }}{% endif %}
{% if edu.courses and edu.courses.size > 0 %}
**Relevant coursework:**
{% for c in edu.courses %}
- {{ c }}
{% endfor %}
{% endif %}

{% endfor %}
{% else %}
_No education entries found._
{% endif %}

## Skills
{% if site.data.cv.skills and site.data.cv.skills.size > 0 %}
- {% for s in site.data.cv.skills %}{{ s }}{% if forloop.last == false %}, {% endif %}{% endfor %}
{% else %}
_No skills listed._
{% endif %}

## Publications
{% if site.data.cv.publications and site.data.cv.publications.size > 0 %}
{% for p in site.data.cv.publications %}
- **{{ p.name }}**, _{{ p.publisher }}_ ({{ p.releaseDate }}) — [link]({{ p.website }})
  - {{ p.summary }}
{% endfor %}
{% else %}
_No publications listed._
{% endif %}

## Presentations
{% if site.data.cv.presentations and site.data.cv.presentations.size > 0 %}
{% for t in site.data.cv.presentations %}
- **{{ t.name }}**, {{ t.event }} ({{ t.date }}) — {{ t.location }}
{% endfor %}
{% else %}
_No presentations listed._
{% endif %}
