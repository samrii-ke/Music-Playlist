# Music-Playlist
 🎵 Simple Music Playlist A relaxing collection of tracks to keep you focused while coding. Perfect for staying in the zone, whether you're writing code, fixing bugs, or just thinking.
//html code
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Music Player</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <a href="#" class="logo">MUSIC-<span>PLATLIST</span></a>
  </header>

  <main>
    <div class="music-continer"></div>
    <div class="music-play" style="display: none;"></div>
  </main>
  <script src="main.js"></script>
</body>
</html>
css code
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
  background-color: #1b1c24;
  color: #fff;
}

header {
  height: 10vh;
  background-color: #1b1c24;
  display: flex;
  align-items: center;
  justify-content: center;
}

.logo {
  font-size: 1.8em;
  font-weight: bold;
  color: #ff6600;
  text-decoration: none;
}

.logo span {
  color: #ff5400;
}

.music-continer {
  padding: 1em;
  display: flex;
  flex-direction: column;
  gap: 1em;
}

.music-box {
  display: flex;
  align-items: center;
  gap: 1em;
  background-color: #292c36;
  padding: 1em;
  border-radius: 1em;
  cursor: pointer;
  transition: background 0.2s ease;
  
}

.music-box:hover {
  background-color: #333640;
  transform: scale(1.01);
}

.image-box {
  width: 80px;
  height: 90px;
  flex-shrink: 0;
  border-radius: 50%;
  overflow: hidden;
  border: 2px solid #ff5100;
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0% { box-shadow: 0 0 0 0 rgba(255, 81, 0, 0.7); }
  70% { box-shadow: 0 0 0 10px rgba(255, 81, 0, 0); }
  100% { box-shadow: 0 0 0 0 rgba(255, 81, 0, 0); }
}

.image-box img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.description {
  flex: 1;
}

.title {
  font-size: 1.2em;
  color: #db7c4e;
}

.music-name {
  font-size: 0.9em;
  color: #fff;
}

.music-play {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #1b1c24;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  padding-top: 2em;
}

.head {
  width: 100%;
  padding: 1em;
  display: flex;
  justify-content: space-between;
  position: fixed;
  top: 0;
}

.musicplay-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1em;
  width: 100%;
  margin-top: 10em;
}

.image-play {
  width: 50%;
  height: 50%;
  border: 4px solid #ff4900;
  border-radius: 50%;
  overflow: hidden;
  margin-top: 1em;
  animation: spin 10s linear infinite;
  position: relative;
  top: -6em;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

.image-play img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
}

.p-title {
  color: #ae7159;
  font-size: 1.5em;
  text-align: center;
}

.p-name {
  color: #ee9673;
  text-align: center;
  font-size: 1em;
}

.all-progress{
  display: flex;
  width: 100vw;
align-items: center;
justify-content : space-between;
  
}
.music-progress {
  width: 80%;
  height: 6px;
  background: #333;
  border-radius: 3px;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  margin-top : 3.5em;
  transition: background 0.3s ease;
  display: flex;
  left: 2em;
}

.progress-bar {
  position: absolute;
  height: 100%;
  background: #ff5100;
  width: 0%;
  border-radius: 3px;
}

.duration {
  display: flex;
  justify-content: space-between;
  width: 100%;
  font-size: 0.9em;
  color: #ccc;
  position: relative;
  top: -3em;
}

.control-panel {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 80%;
  gap: 1em;
  flex-wrap: wrap;
}

.volume-container {
  display:  none;
  align-items: center;
  gap: 0.5em;
  flex: 1;
  width: 15%;
  position: relative;
  top: -3em;
  left: 5em;
}

.volume-icon {
  color: #ff5100;
  font-size: 1.2em;
}

input.volume {
  flex: 1;
  appearance: none;
  height: 6px;
  background: linear-gradient(to right, #ff5100 100%, #444 0%);
  border-radius: 3px;
  outline: none;
  transition: background 0.3s;
}

input.volume::-webkit-slider-thumb {
  appearance: none;
  width: 14px;
  height: 14px;
  background: #ff5100;
  border-radius: 50%;
  cursor: pointer;
  border: none;
}
.volume-iconc {
  align-items: center;
  position :relative;
  top: 1.5em;
  
}
.volume-iconc svg:hover{
  fill: rgba(255, 84, 0, 1);
}
.music-control {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 4em;
  flex: 1;
  width: 90%;
  position: relative;
  top: -1.8em;
}

.play, .prev, .next {
  cursor: pointer;
  font-size: 1.8em;
  transition: transform 0.2s ease;
}

.play:hover, .prev:hover, .next:hover {
  transform: scale(1.2);
}

.previous, .theme {
  font-size: 2em;
  border:  solid #ff4200;
  border-radius: 50%;
  box-shadow: 3px 6px 12px rgba(0, 0, 0, 1);
  padding: 0.3em;
}
.next,
.play,
.prev{
  box-shadow : 3px 6px 9px rgba(0, 0, 0, 1);
  border: solid rgba(255, 55, 0, 1);
  border-radius : 50%;
  padding: 0.3em;
  
}


@media (min-width: 60em) {
  .music-control {
    gap: 1em;
  }

  .control-panel {
    flex-direction: column;
    align-items: center;
  }

  .volume-container {
    width: 15%;
  }
  .logo{
    font-size: 4em;
  }
  .music-continer{
    display: grid;
    grid-template-columns : repeat(2,1fr);
    position: relative;
    overflow: scroll;
  }
  .image-box {
    width: 300px;
    height: 250px;
  }
  .music-box{
    width: 30em;
    height: 30em;
    display: grid;
    grid-template-rows: repeat(3,1fr);
    align-items: center;
    justify-content: center;
    text-align : center;
  }
.title{
  font-size : 3em;
  
}
.music-name{
  font-size : 2.5em;
}
.musicPlay{
     width: 100vw;
     height: 100vh;
   }
   .p-title {
     font-size: 4em;
     margin-top: 2em;
   }
   .p-name{
     font-size: 3em;
     margin-top: 1em;
   }
  @keyframes pulse {
  0% { box-shadow: 0 0 0 10px rgba(255, 81, 0, 0.7); }
  70% { box-shadow: 0 0 0 30px rgba(255, 81, 0, 0); }
  100% { box-shadow: 0 0 0 10px rgba(255, 81, 0, 0); }
}
.previous{
   font-size: 5em;
}
.theme svg{
  width: 80px;
  height: 80px;
  padding-top: 1em;
}
.image-play{
  margin-top: 10vh;
  
}
.pimg{
  width: 100%;
  height: 100%;

}
.all-progress{
  
}
.music-progress{
  height: 12px ;
  position: relative;
   left: 3em;

}
.volume-iconc svg{
   width: 90px;
   height: 90px;
}
.current-duration, 
.music-duration{
  font-size: 2.5em;
  top: 1em;
}
.music-control{
  margin-top: 4em;
  left: 3em;
}
.play{
  border : 4px solid rgba(255, 84, 0, 1);
}
.play svg{
  width: 150px ;
  height: 150px;
  
}
.prev,
.next{
  font-size: 5em;
  border : 4px solid rgba(255, 84, 0, 1);
}
.volume-container{
  margin-top: 3em;
}
.volume-icon svg{
  width: 100px;
height: 100px;
}
.duration{
  width: 100vw;
  padding-left : 2em;
}
.music-duration{
  padding-right : 3.7em;
}
.input.volume{
  height: 50px;
}
.input.volume::-webkit-slider-thumb{
  height: 50px;

}
//JavaScript  code
const musicContainer = document.querySelector('.music-continer');
const musicPlay = document.querySelector('.music-play');

let musics = [
  {
  image: "p4.jpg",
  title: "Liar",
  name: "Camila Cabello",
  audio: "a1.mp3"
},
{
  image: "p3.jpg",
  title: "Cry for Me",
  name: "Camila Cabello",
  audio: "a2.mp3"
},
{
  image: "p5.jpg",
  title: "Perfect to me",
  name: "Victoria Anderson",
  audio: "a3.mp3"
},
{
  image: "p2.jpg",
  title: "NO DOUBT",
  name: "Camila Cabello",
  audio: "a4.mp3"
},
{
  image: "p6.jpg",
  title: "Not Like Us",
  name: "Kandrik lamar",
  audio: "a5.mp3"
},
{
  image: "p7.jpg",
  title: "Anyone",
  name: "justin Bieber",
  audio: "a6.mp3"
},
{
  image: "p1.jpg",
  title: "Find you Again",
  name: "Camila Cabello",
  audio: "a7.mp3"
},
{
  image: "p8.jpg",
  title: "Last Last",
  name: "Burna Boy",
  audio: "a8.mp3"
},
{
  image: "p1.jpg",
  title: "Psychofreak",
  name: "Camila Cabello",
  audio: "a9.mp3"
},
{
  image: "p8.jpg",
  title: "on the low",
  name: "Burna Boy",
  audio: "a10.mp3"
}
];

musics.forEach((music, index) => {
  const box = document.createElement('div');
  box.className = 'music-box';
  box.dataset.index = index;
  box.innerHTML = `
    <div class="image-box">
      <img src="${music.image}" class="img">
    </div>
    <div class="description">
      <h1 class="title">${music.title}</h1>
      <p class="music-name">${music.name}</p>
    </div>
  `;
  musicContainer.appendChild(box);
});

let currentIndex = 0;
let audio = new Audio();
let isPlaying = false;

function showPlayer(index) {
  currentIndex = index;
  const music = musics[index];

  const playSVG = `
    <svg xmlns="http://www.w3.org/2000/svg" height="50px" viewBox="0 -960 960 960" width="50px" fill="#e3e3e3">
      <path d="m380-300 280-180-280-180v360Z"/>
    </svg>`;

  const pauseSVG = `
    <svg xmlns="http://www.w3.org/2000/svg" height="50px" viewBox="0 -960 960 960" width="50px" fill="#e3e3e3">
      <path d="M360-320h80v-320h-80v320Zm160 0h80v-320h-80v320Z"/>
    </svg>`;

  musicPlay.innerHTML = `
    <div class="head">
      <div class="previous"><=</div>
      <div class="theme">
        <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960" width="24px" fill="#e3e3e3">
          <path d="M400-120q-66 0-113-47t-47-113q0-66 47-113t113-47q23 0 42.5 5.5T480-418v-422h240v160H560v400q0 66-47 113t-113 47Z"/>
        </svg>
      </div>
    </div>
    <div class="musicplay-box">
      <div class="image-play"><img src="${music.image}" class="pimg"></div>
      <h1 class="p-title">${music.title}</h1>
      <p class="p-name">${music.name}</p>
      <div class="all-progress">
      <div class="music-progress"><div class="progress-bar"></div></div>
        <i class="volume-iconc">
          <svg xmlns="http://www.w3.org/2000/svg" height="34px" viewBox="0 -960 960 960" width="34px" fill="#e3e3e3">
            <path d="M200-360v-240h160l200-200v640L360-360H200Z"/>
          </svg>
      </div>
      </div>
      <div class="duration">
        <div class="current-duration">0:00</div>
        <div class="music-duration">0:00</div>
      </div>
     <div class="volume-container">
        <i class="volume-icon">
          <svg xmlns="http://www.w3.org/2000/svg" height=" 35px" viewBox="0 -960 960 960" width="35px" fill="#e3e3e3">
            <path d="M200-360v-240h160l200-200v640L360-360H200Z"/>
          </svg>
        </i>
        <input type="range" class="volume" min="0" max="1" step="0.01" value="1">
      </div>
      <div class="music-control">
        <div class="prev">⏮</div>
        <div class="play">${playSVG}</div>
        <div class="next">⏭</div>
      </div> </div>
      </div>
    
  `;

  audio.src = music.audio;
  audio.load();
  const musicC = document.querySelector('.volume-container');
  const volumeC= document.querySelector('.volume-iconc')
  const volumeCl= document.querySelector('.volume-icon')
  const playBtn = musicPlay.querySelector('.play');
  const prevBtn = musicPlay.querySelector('.prev');
  const nextBtn = musicPlay.querySelector('.next');
  const progressBar = musicPlay.querySelector('.progress-bar');
  const progressArea = musicPlay.querySelector('.music-progress');
  const currentTimeEl = musicPlay.querySelector('.current-duration');
  const durationEl = musicPlay.querySelector('.music-duration');
  const volumeSlider = musicPlay.querySelector('.volume');
  const closeBtn = musicPlay.querySelector('.previous');

  function updateVolumeFill() {
    const val = volumeSlider.value * 100;
    volumeSlider.style.background = `linear-gradient(to right, #ff5100 ${val}%, #444 ${val}%)`;
  }
  volumeC.addEventListener('click',()=>{
    musicC.style. display='flex';
  });
  volumeCl.addEventListener('click', () => {
  musicC.style.display = 'none';
});

  closeBtn.addEventListener('click', () => {
    audio.pause();
    musicPlay.style.display = 'none';
  });

  playBtn.addEventListener('click', () => {
    if (isPlaying) {
      audio.pause();
      playBtn.innerHTML = playSVG;
    } else {
      audio.play();
      playBtn.innerHTML = pauseSVG;
    }
    isPlaying = !isPlaying;
  });

  prevBtn.addEventListener('click', () => {
    loadTrack((currentIndex - 1 + musics.length) % musics.length);
  });

  nextBtn.addEventListener('click', () => {
    loadTrack((currentIndex + 1) % musics.length);
  });

  volumeSlider.addEventListener('input', () => {
    audio.volume = volumeSlider.value;
    updateVolumeFill();
  });
  updateVolumeFill();

  let isDragging = false;
  progressArea.addEventListener('mousedown', () => isDragging = true);
  window.addEventListener('mouseup', () => isDragging = false);
  progressArea.addEventListener('mousemove', (e) => {
    if (isDragging) {
      const width = progressArea.clientWidth;
      const offsetX = e.offsetX;
      audio.currentTime = (offsetX / width) * audio.duration;
    }
  });
  progressArea.addEventListener('click', (e) => {
    const width = progressArea.clientWidth;
    const clickX = e.offsetX;
    audio.currentTime = (clickX / width) * audio.duration;
  });

  audio.addEventListener('loadeddata', () => {
    const min = Math.floor(audio.duration / 60);
    let sec = Math.floor(audio.duration % 60);
    if (sec < 10) sec = '0' + sec;
    durationEl.textContent = `${min}:${sec}`;
  });

  audio.addEventListener('timeupdate', () => {
    const progressPercent = (audio.currentTime / audio.duration) * 100;
    progressBar.style.width = `${progressPercent}%`;

    const min = Math.floor(audio.currentTime / 60);
    let sec = Math.floor(audio.currentTime % 60);
    if (sec < 10) sec = '0' + sec;
    currentTimeEl.textContent = `${min}:${sec}`;
  });

  audio.addEventListener('ended', () => {
    loadTrack((currentIndex + 1) % musics.length);
  });
  musicPlay.style.display = 'flex';
  audio.play();
  isPlaying = true;
  playBtn.innerHTML = pauseSVG;
}
function loadTrack(index) {
  audio.pause();
  showPlayer(index);
}
document.querySelectorAll('.music-box').forEach(box => {
  box.addEventListener('click', () => {
    const index = parseInt(box.dataset.index);
    showPlayer(index);
  });
});
