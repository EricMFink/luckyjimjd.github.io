---
layout: music
permalink: /music/
title: Music
---

{% for song in site.data.songs %}
	
<p>{{ song.title }} <a href="../assets/music/{{ song.file }}"><i class="{{ network.title }}"></i></a></p>

{% endfor %}
