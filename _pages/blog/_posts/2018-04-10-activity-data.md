---
layout: post
title:  "activity data"
date:   2018-04-10 16:16:01 -0600
categories: data
permalink: /blog/activity-data
---

see: https://jekyllrb.com/docs/datafiles/

<ul>
{% for activity in site.data.activities %}
  <li> I went {{activity.activity}} in {{activity.location}} for {{activity.duration}} minutes.
  </li>
{% endfor %}
</ul>