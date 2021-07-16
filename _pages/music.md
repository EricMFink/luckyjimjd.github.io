---
layout: music
permalink: /music/
title: Music
---

{% include embed-audio.html src="../assets/music/fireworks.ogg" %}


{% for song in site.data.songs %}
	
<p>{{ song.title }} <a href="../assets/music/{{ song.file }}"><i class="fas fa-music"></i></a></p>

{% endfor %}
