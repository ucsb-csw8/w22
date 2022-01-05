---
layout: page
title: Schedule
description: The weekly event schedule.
---

# Weekly Schedule

See the [Schedule and Roadmap]({{site.url}}/{{site.baseurl}}/success/#time-management-and-scheduling) suggestions. 

Use the same Zoom link for lab and office hours as you use for lecture
 or [schedule a meeting with Prof. K using this link](https://calendar.google.com/calendar/u/0/selfsched?sstoken=UUFjZExlYWxLMkdRfGRlZmF1bHR8NTZmMGZmY2IyYjFmZTVmMmNmNWQ0YmUxZjQ2MWUwOGY)

{% for schedule in site.schedules %}
{{ schedule }}
{% endfor %}
