---
layout: music
permalink: /music/
title: Music
---

{% for song in site.data.songs %}

<div class="row">

<div class="column">
<div class="card">![](../assets/music/AlbumCover1.png)</div>
</div>

<div class="column">
{% for song in site.data.songs %}
<p>{{ song.title }}</p>
{% endfor %}
</div>

<div class="column">
{% for song in site.data.songs %}
<p>{% include embed-audio.html src="../assets/music/{{ song.file }" %}</p>
{% endfor %}
</div>

</div>

<p>{{ song.title }} {% include embed-audio.html src="../assets/music/{{ song.file }" %}</p>


