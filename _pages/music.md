---
layout: music
permalink: /music/
title: Music
---


![](../assets/music/AlbumCover1.png)

{% for song in site.data.songs %}
	
<p>{{ song.title }} {% include embed-audio.html src="../assets/music/{{ song.file }" %}</p>

{% endfor %}
