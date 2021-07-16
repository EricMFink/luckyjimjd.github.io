---
layout: music
permalink: /music/
title: Music
---

<div class="grid-x grid-padding-x">
<div class="large-12 medium-12 small-12 cell">


    <div id="single-song-player">
      <img data-amplitude-song-info="cover_art_url" amplitude-main-song-info="true"/>
      <div class="bottom-container">
        <progress class="amplitude-song-played-progress" id="song-played-progress"></progress>

        <div class="time-container">
          <span class="current-time">
            <span class="amplitude-current-minutes"></span>:<span class="amplitude-current-seconds"></span>
          </span>
          <span class="duration">
            <span class="amplitude-duration-minutes"></span>:<span class="amplitude-duration-seconds"></span>
          </span>
        </div>

        <div class="control-container">
          <div class="amplitude-play-pause" id="play-pause"></div>
          <div class="meta-container">
            <span data-amplitude-song-info="name" class="song-name"></span>
            <span data-amplitude-song-info="artist"></span>
          </div>
        </div>
      </div>
    </div>


</div>
</div>

<script>
  Amplitude.init({
    "songs": [
      {
        "name": "Return of the Grievous Angel",
        "artist": "Ulrich Kvetcher",
        "album": "Too Old for Teen Angst, Too Young to Die",
        "url": "../assets/music/GrievousAngel.ogg",
        "cover_art_url": "../assets/music/AlbumCover1.png"
      }
    ]
  });
</script>
