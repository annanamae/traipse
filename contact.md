---
layout: default
title: Contact
permalink: /contact/
---

# Contact

The best way to reach us is by email:

<p><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>

You can also find us here:

- {% if site.social.github %}[GitHub](https://github.com/{{ site.social.github }}){% else %}GitHub (add `social.github` in `_config.yml`){% endif %}
- {% if site.social.twitter %}[Twitter](https://twitter.com/{{ site.social.twitter }}){% else %}Twitter (add `social.twitter` in `_config.yml`){% endif %}
- {% if site.social.linkedin %}[LinkedIn](https://www.linkedin.com/in/{{ site.social.linkedin }}){% else %}LinkedIn (add `social.linkedin` in `_config.yml`){% endif %}
