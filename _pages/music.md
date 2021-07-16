---
layout: music
permalink: /music/
title: Music
---

<div class="flex-container">

<div>
<img src="../assets/music/AlbumCover1.png" alt="Album Cover" width="90%" >
</div>

<div>
{% for song in site.data.songs %}
<div class="flex-container">
{{ song.title }}
</div>
{% endfor %}
</div>

<div>
{% for song in site.data.songs %}
<div class="flex-container">{% include embed-audio.html src="../assets/music/{{ song.file }" %}
</div>
{% endfor %}
</div>  
  
</div>

