<!DOCTYPE html>
<html>
{% include head.html %}

<body class="fullwidth">

{% include header.html %}

<div class="page-container">

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

window.onkeydown = function(e) {
return !(e.keyCode == 32);
};

/*
Handles a click on the down button to slide down the playlist.
*/
document.getElementsByClassName('down-header')[0].addEventListener('click', function(){
var list = document.getElementById('list');

list.style.height = ( parseInt( document.getElementById('flat-black-player-container').offsetHeight ) - 135 ) + 'px';

document.getElementById('list-screen').classList.remove('slide-out-top');
document.getElementById('list-screen').classList.add('slide-in-top');
document.getElementById('list-screen').style.display = "block";
});

/*
Handles a click on the up arrow to hide the list screen.
*/
document.getElementsByClassName('hide-playlist')[0].addEventListener('click', function(){
document.getElementById('list-screen').classList.remove('slide-in-top');
document.getElementById('list-screen').classList.add('slide-out-top');
document.getElementById('list-screen').style.display = "none";
});

/*
Handles a click on the song played progress bar.
*/
document.getElementById('song-played-progress').addEventListener('click', function( e ){
var offset = this.getBoundingClientRect();
var x = e.pageX - offset.left;

Amplitude.setSongPlayedPercentage( ( parseFloat( x ) / parseFloat( this.offsetWidth) ) * 100 );
});

document.querySelector('img[data-amplitude-song-info="cover_art_url"]').style.height = document.querySelector('img[data-amplitude-song-info="cover_art_url"]').offsetWidth + 'px';

Amplitude.init({
"songs": [
{% for song in site.data.songs %}
  {		
    "name": "{{ song.title }}",
    "url": "../assets/music/{{ song.url }}",
    "cover_art_url": "../assets/music/{{ song.art }}"
  }
{% endfor %}
]
});
</script>

</div>

{% include open-embed.html %}
{% include footer.html %}
{% include hemline.html %}

</body>

</html>

