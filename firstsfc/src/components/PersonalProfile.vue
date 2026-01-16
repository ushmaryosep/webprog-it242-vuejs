<template>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Joshmar L. Clavero | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">
  <link rel="stylesheet" href="components/css/style.css?version=0.1">
</head>

<body>

<header>
  <div class="hero-text">
    <h1>Hi, I am <span>Josh</span></h1>
    <h3>Joshmar L. Clavero</h3>
    <p>A BSIT student passionate about technology, creativity, and building meaningful digital experiences.</p>
    <div class="socials"> 
      <a href="https://www.instagram.com/ushmaryosep/" target="_blank"><i class="fab fa-instagram"></i></a> 
      <a href="https://www.linkedin.com/in/joshmar-clavero-8b1912322/" target="_blank"><i class="fab fa-linkedin"></i></a> 
      <a href="https://github.com/ushmaryosep" target="_blank"><i class="fab fa-github"></i></a> <a href="https://www.facebook.com/joshmar.clavero" target="_blank"><i class="fab fa-facebook"></i></a> 
    </div> 
  </div>
  <div class="hero-image">
    <img src="https://raw.githubusercontent.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/refs/heads/feature/2_JC_customize_my_website/PFP1.png">
  </div>
</header>

<section id="about">
  <h2>About Me</h2>
  <div class="content-box">
    <p>
      My interest in computers started at a young age, driven by curiosity and fascination with how digital systems work.
      Over time, this curiosity evolved into a genuine passion for programming and animation, where I enjoyed seeing ideas
      transform into functional and visual outputs. Alongside this, I developed strong skills in graphic design, allowing
      me to blend technical knowledge with creativity. Today, I continue to sharpen my abilities in IT while exploring
      opportunities where design, technology, and innovation intersect.
    </p>
    <div class="content-icon"><i class="fa-solid fa-user"></i></div>
  </div>
</section>

<section id="gallery">
  <h2>Picture Gallery</h2>

  <div class="gallery-menu">
    <button class="active" onclick="showGallery('me', this)">Me</button>
    <button onclick="showGallery('family', this)">Family & Friends</button>
    <button onclick="showGallery('others', this)">Others</button>
  </div>

  <div id="me" class="gallery-section active">
    <div class="gallery-grid">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/ME1.jpg?raw=true" onclick="openModal(this.src)">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/ME2.jpg?raw=true" onclick="openModal(this.src)">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/ME3.jpg?raw=true" onclick="openModal(this.src)">
    </div>
  </div>

  <div id="family" class="gallery-section">
    <div class="gallery-grid">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/FNF1.jpg?raw=true" onclick="openModal(this.src)">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/FNF2.jpg?raw=true" onclick="openModal(this.src)">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/FNF3.jpg?raw=true" onclick="openModal(this.src)">
    </div>
  </div>

  <div id="others" class="gallery-section">
    <div class="gallery-grid">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/O2.jpg?raw=true" onclick="openModal(this.src)">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/O1.jpg?raw=true" onclick="openModal(this.src)">
      <img src="https://github.com/ushmaryosep/WEBPROG-IT242-HTML-Lessons/blob/feature/2_JC_customize_my_website/O3.png?raw=true" onclick="openModal(this.src)">
    </div>
  </div>
</section>

<!-- Modal -->
<div id="modal" class="modal">
  <span class="modal-close" onclick="closeModal()">&times;</span>
  <img class="modal-content" id="modal-img">
</div>

<script>
  function showGallery(id, btn) {
    document.querySelectorAll('.gallery-section').forEach(s => s.classList.remove('active'));
    document.getElementById(id).classList.add('active');

    document.querySelectorAll('.gallery-menu button').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
  }

  function openModal(src) {
    document.getElementById('modal-img').src = src;
    document.getElementById('modal').style.display = "block";
  }

  function closeModal() {
    document.getElementById('modal').style.display = "none";
  }
</script>

</body>
</html>
</template>