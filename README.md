<!DOCTYPE html>
<html>
<meta charset='UTF-8' />
<meta content='width=device-width, initial-scale=1, user-scalable=1, minimum-scale=1, maximum-scale=5'
  name='viewport' />
<meta content='IE=edge' http-equiv='X-UA-Compatible' />

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:wght@400;700&display=swap" rel="stylesheet">

<script src="https://cdn.jsdelivr.net/npm/sweetalert2@11.0.19/dist/sweetalert2.all.min.js"></script>
<script src="https://unpkg.com/typeit@8.7.0/dist/index.umd.js"></script>
<!--<link href="https://feeldreams.github.io/dibacayuk/style.css" rel="stylesheet" type="text/css" />-->
<script src="https://kit.fontawesome.com/4f3ce16e3e.js" crossorigin="anonymous"></script>
<script src="https://unpkg.com/scrollreveal"></script>

<head>
  <title>Script HTML buat Kamu</title>
  <meta name="description" content="HTML Feeldream Repl Co">
  <!-- 
  Made with love by Rayys!

     Blog: feeldream.id
     Instagram: @rayyarrr
     TikTok: @feelthisray
     Email: rayyar73@gmail.com

  Thanks to all <3
-->
</head>
<style>
  :root {
    --gaya-font: 'Quicksand', sans-serif;
    --gaya-font2: 'Nunito Sans', sans-serif;
    --gaya-font3: 'Dancing Script', sans-serif;
  }

  body {
    background: #000;
    font-family: var(--gaya-font);
    margin: 0;
  }

  #bodyblur {
    animation: jj 7s infinite;
    opacity: .7;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: -1;
    transition: all 1s ease;
  }

  #wallpaper {
    width: 100%;
    height: 100%;
    transform: scale(2);
    transition: all 1.7s ease;
  }

  @keyframes jj {
    0% {
      transform: scale(1.2);
    }

    50% {
      transform: scale(1.5);
    }

    100% {
      transform: scale(1.2);
    }
  }

  .parallax {
    z-index: 0;
    background-image: url('https://feeldreams.github.io/akuharap/6.jpg');
    height: 100vh;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .parallax>* {
    display: flex;
    z-index: 1;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-shadow: 0px 2px 2px rgba(0, 0, 0, .8);
  }

  #beneranblur {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, .75);
    -webkit-backdrop-filter: blur(0px);
    backdrop-filter: blur(0px);
    transition: all 3s ease;
  }

  .parallax .konten {
    position: absolute;
    top: 20%;
    width: 100%;
    z-index: 99;
    color: white
  }

  section {
    position: relative;
    z-index: 99;
    padding: 1em;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-shadow: 0px 2px 2px rgba(0, 0, 0, .8);
    border-top: 2px dashed #fff
  }

  section:nth-child(even) {
    background: #21243A;
    color: white
  }

  section:nth-child(odd) {
    background: #18122B;
    color: white
  }

  img {
    width: 90px;
    height: 90px;
    background: rgba(255, 255, 255, 0.7);
    box-shadow: 0 4px 30px rgba(255, 255, 255, 0.3);
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.3);
    border-radius: 10%;
    padding: 10px;
    margin-bottom: 25px
  }

  h1 {
    font-size: 2rem;
  }

  .lingkar {
    font-weight: 400;
    border-bottom: 1px solid #FF0900;
  }

  h1,
  h2,
  h3 {
    margin: 0;
    text-align: center;
    margin: 1rem 0;
  }

  p {
    font-size: 15px;
    font-family: var(--gaya-font2);
    text-align: center
  }

  a {
    color: white;
    text-decoration: none;
    transition: all 0.3s ease-in-out;

    &:hover,
    &:focus,
    &:active {
      color: #f1e8d9;
    }
  }

  #hsatu,
  #foto {
    transition: all .3s ease
  }

  #judulakhir {
    font-size: 25px;
    font-family: var(--gaya-font3);
  }

  #kalimatakhir {
    margin-right: 50px;
    margin-left: 50px;
    font-size: 15px;
    font-family: var(--gaya-font2);
  }

  .tipeA {
    font-family: var(--gaya-font);
  }

  svg {
    vertical-align: middle;
    width: 22px;
    height: 22px;
    fill: #fff
  }

  .menu {
    position: fixed;
    bottom: 10vh;
    width: 100%;
    z-index: 999;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all .3s ease
  }

  .tombol {
    background-color: rgba(255, 255, 255, .25);
    border-radius: 50px;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 45px;
    height: 45px;
    -webkit-transition: all .2s ease-out;
    transition: all .2s ease-out
  }

  .tombol svg {
    margin: auto;
    fill: #fff
  }

  .fa-heart {
    opacity: .3;
    color: white;
    font-size: 20px;
    position: fixed;
    animation: heartMove linear 1;
    top: -10vh;
    z-index: 999;
  }

  @keyframes heartMove {
    0% {
      transform: translateY(-10vh);
    }

    100% {
      transform: translateY(100vh);
    }
  }
</style>

<body onclick="tes()">

  <!-- Ganti Audio di sini -->
  <audio src="https://feeldreams.github.io/audio/nightchanges.mp3" id="linkmp3" class="sembunyi"></audio>

  <div id="bodyblur">
    <!-- Wallpaper --><img src="https://feeldreams.github.io/pics/awan.jpg" id="wallpaper" />
  </div>

  <div class="parallax">
    <div id="beneranblur"></div>
    <div class="konten">
      <img class="fade-in" src="https://feeldreams.github.io/pusn.gif" />
      <h1 class="title">Hallo Hafsa!</h1>
      <p class="fade-in">Aku ada pesan buat kamu </p>
    </div>
  </div>

  <section>
    <h2 class="title">Semangat Ngejalani<br>Harinya yaa ðŸ¥³ðŸ¥³ðŸ¥³</h2>
    <p class="slide-right">Aku harap<b class="lingkar">mood kamu jadi makin baik</b> lagi ya.<br>Jangan ovt dan sedihh
      yaaa<br>aku yakin kamu bisa laluin semuanya dan aku harap kamu bisa pulih dari hal hal yang ga mau kamu bicarakan
    </p>
  </section>

  <section>
    <h1 class="title slide-right">Jangan menyerah yaa Karena..</h1>
    <p class="slide-up">Di setiap adanya <b class="lingkar">kesulitan</b>,<br>pasti akan ada kemudahan kokðŸ˜</p>
  </section>

  <section>
    <img class="fade-in" src="https://feeldreams.github.io/ciumin.gif" />
    <h2 class="title">Hari ini,besok, dan selanjutnya aku harap semoga hari harinya berjalan lancar yaa âœ¨</h2>
    <p class="slide-right">Kamu kalau mau cerita,bisa kok cerita ke aku aja pasti aku dengerinn,<br><b
        class="lingkar">dan kamu ga bolee terlalu sering begadangg yaaa!</b></p>
    <p class="slide-up">dan Kamu juga jangan nunda nunda makann ya biar ga sakitt apalagii kamu ada ikut aktivitas lagii
      dan juga harapp kita bisaa ketemuu dan ga bakal lostcontact</p>
  </section>

  <section id="iniakhir">
    <h1 id="hsatu" class="slide-up">Terakhir...</h1>
    <img id="foto" class="flip" src="https://feeldreams.github.io/ngumpet.gif" />
    <p id="kalimat" class="flip">Coba deh klik ini ðŸ˜Š</p>

    <h1 id="judulakhir"></h1>
    <p id="kalimatakhir"></p>
  </section>

  <div id="initom" class="menu">
    <a class='tombol'>
      <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-arrow-down"
        viewBox="0 0 16 16">
        <path fill-rule="evenodd"
          d="M8 1a.5.5 0 0 1 .5.5v11.793l3.146-3.147a.5.5 0 0 1 .708.708l-4 4a.5.5 0 0 1-.708 0l-4-4a.5.5 0 0 1 .708-.708L7.5 13.293V1.5A.5.5 0 0 1 8 1z" />
      </svg>
    </a>
  </div>

  <script>
    judulakhir = "Terimakasih ya Hafsa udah bertahan sampai sekarang";
    kalimatakhir = "Kamu gaboleh sedihÂ² ya,<br>.<br>Terima kasih sudah berjuang hingga saat ini,kamu hebat pasti adek adek kamu bangga punya kaka kaya kamu dan keluarga kamu pasti bangga,Im always proud of you Hafsa .<br><br>I'm always support you,<br><b>SEMANGAT yaa! jalaninn hari harinya,jangan sering kecapeann yaa,kamu jugaa jaga kesehatannyaaaâ¤ï¸</b>";

    const body = document.querySelector("body"); audio = new Audio('' + linkmp3.src); function berjatuhan() {const heart = document.createElement("div"); heart.className = "fas fa-heart"; heart.style.left = (Math.random() * 90) + "vw"; heart.style.animationDuration = (Math.random() * 3) + 2 + "s"; body.appendChild(heart);} setInterval(function name(params) {var heartArr = document.querySelectorAll(".fa-heart"); if (heartArr.length > 100) {heartArr[0].remove()} }, 100);
    ScrollReveal({reset: true});
    ScrollReveal().reveal(".show-once", {reset: false});
    ScrollReveal().reveal(".title", {duration: 2500, origin: "top", distance: "50px", easing: "cubic-bezier(0.5, 0, 0, 1)", rotate: {x: 20, z: -10}});
    ScrollReveal().reveal(".fade-in", {delay: 200, duration: 2500, move: 0});
    ScrollReveal().reveal(".scaleUp", {duration: 2500, scale: 0.85});
    ScrollReveal().reveal(".flip", {delay: 500, duration: 2000, rotate: {x: 20, z: 20}});
    ScrollReveal().reveal(".slide-right", {duration: 1000, origin: "left", distance: "300px", easing: "ease-in-out"});
    ScrollReveal().reveal(".slide-up", {duration: 1500, origin: "bottom", distance: "100px", easing: "cubic-bezier(.37,.01,.74,1)", opacity: 0, scale: 0.5});

    fungsi = 0; fungsiklik = 0;
    document.getElementById("iniakhir").onclick = function () {
      if (fungsiklik == 0) {
        hsatu.style = "opacity:0";
        foto.style = "opacity:0";
        kalimat.style = "opacity:0";
        iniakhir.style = "background:none";
        wallpaper.style = "transform: scale(1)";
        fungsiklik = 1;
        setTimeout(katajudul, 300)
      }
    }

    function katajudul() {
      hsatu.style = "display:none";
      foto.style = "display:none";
      kalimat.style = "display:none";
      new TypeIt("#judulakhir", {
        strings: ["" + judulakhir], startDelay: 50, speed: 50, cursor: false,
        afterComplete: function () {
          judulakhir.innerHTML = judulakhir;
          setTimeout(katakata, 300);
        },
      }).go();
    }
    function katakata() {
      new TypeIt("#kalimatakhir", {
        strings: ["" + kalimatakhir], startDelay: 50, speed: 50, cursor: false,
        afterComplete: function () {
          kalimatakhir.innerHTML = kalimatakhir;
          setInterval(berjatuhan, 200);
        },
      }).go();
    }
    let tinggi = iniakhir.offsetHeight;
    console.log(tinggi);
    function tes() {
      window.scrollBy({top: tinggi, behavior: 'smooth'});
      fungsi += 1;
    }
    window.scrollTo(0, 0);

    document.addEventListener('DOMContentLoaded', function (e) {
      document.addEventListener('scroll', function (e) {
        let documentHeight = document.body.scrollHeight;
        let currentScroll = window.scrollY + window.innerHeight;
        // When the user is [modifier]px from the bottom, fire the event.
        let modifier = 200;
        if (currentScroll + modifier > documentHeight) {
          console.log('You are at the bottom!');
          initom.style = "opacity:0;bottom:0";
        } else {
          initom.style = "";
        }
      })
    })
  </script>
</body>

</html>
