---
layout: music
permalink: /music/
title: Music
---

<div class="row">

<div class="column">
<div class="card">
<img src="../assets/music/AlbumCover1.png" alt="Album Cover" >
</div>
</div>

<div class="column">
<div class="card">
{% for song in site.data.songs %}
<p>{{ song.title }}</p>
{% endfor %}
</div>
</div>

<div class="column">
<div class="card">
{% for song in site.data.songs %}
<p>{% include embed-audio.html src="../assets/music/{{ song.file }" %}</p>
{% endfor %}
</div>
</div>

</div>



