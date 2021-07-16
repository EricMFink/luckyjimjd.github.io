---
layout: music
permalink: /music_BAK/
title: Music
---

<div class="container">
  <div class="row">
    <div class="col big-box">
      <img src="../assets/music/AlbumCover1.png" alt="Album Cover" >
    </div>

    <div class="col">
		{% for song in site.data.songs %}
    		<div class="row">
    			<div class="col mini-box">{{ song.title }}</div>
    			<div class="col mini-box">{% include embed-audio.html src="../assets/music/{{ song.file }" %}</div>
    		</div>
		{% endfor %}
    </div>

  </div>
</div>