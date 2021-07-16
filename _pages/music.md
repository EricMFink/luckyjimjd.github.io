---
layout: music
permalink: /music/
title: Music
---

<div class="row">

<div class="column">
<img src="../assets/music/AlbumCover1.png" alt="Album Cover" width="25%" >
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




