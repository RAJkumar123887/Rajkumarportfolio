<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#0b0d10">
<title>Muddasani Rajkumar · Actor & Assistant Director</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300..700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<style>
  * { margin:0; padding:0; box-sizing:border-box; }
  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    background:#0b0d10; color:#eef2f6; line-height:1.5; min-height:100vh;
    padding: 1rem; display:flex; justify-content:center; align-items:flex-start;
    background-image: radial-gradient(circle at 20% 20%, rgba(245,197,66,.03) 0%, transparent 40%),
                      radial-gradient(circle at 80% 70%, rgba(245,197,66,.02) 0%, transparent 50%);
  }
  .page {
    max-width:900px; width:100%; padding:2rem 1.5rem;
    background:rgba(18,22,28,.92); border-radius:2.5rem;
    border:1px solid rgba(245,197,66,.1);
    box-shadow: 0 30px 60px -20px rgba(0,0,0,.9);
  }
  header { display:flex; flex-wrap:wrap; align-items:center; gap:1.5rem;
           padding-bottom:1.5rem; margin-bottom:1.5rem;
           border-bottom:1.5px solid rgba(245,197,66,.2); }
  .profile-pic {
    width:120px; height:120px; border-radius:50%; object-fit:cover;
    border:3.5px solid #f5c542; background:#1e222a; flex-shrink:0;
    box-shadow: 0 12px 24px -8px rgba(245,197,66,.25);
  }
  h1 {
    font-size:2.4rem; font-weight:700; line-height:1.1; letter-spacing:-.02em;
    background:linear-gradient(to right,#fff,#f5e6b0);
    -webkit-background-clip:text; background-clip:text; color:transparent;
  }
  .tagline { color:#b0b8c5; font-size:1.1rem; display:flex; align-items:center; gap:6px; margin-top:.3rem; }
  .tagline i { color:#f5c542; }
  .details { display:flex; flex-wrap:wrap; gap:.6rem 1.5rem; margin-top:.8rem; color:#cbd5e1; font-size:.95rem; }
  .details span { display:flex; align-items:center; gap:6px; }
  .details i { color:#f5c542; width:16px; text-align:center; }
  h2 {
    font-size:1.6rem; font-weight:600; margin:2rem 0 1rem;
    display:flex; align-items:center; gap:10px;
  }
  h2 i { color:#f5c542; width:28px; }
  h2::after { content:''; flex:1; height:1.5px; background:linear-gradient(to right,#f5c542,transparent); margin-left:8px; }
  .about {
    background:rgba(30,35,45,.7); padding:1.5rem; border-radius:1.6rem;
    border-left:5px solid #f5c542; color:#d6dee8; font-size:1rem;
  }
  .about p { margin-bottom:.9rem; }
  .about p:last-child { margin-bottom:0; }
  .about i { color:#f5c542; margin-right:6px; }
  .about strong { color:#f5e6b0; }
  .gallery {
    display:grid; grid-template-columns:repeat(auto-fit, minmax(150px,1fr));
    gap:1rem;
  }
  .gallery img {
    width:100%; aspect-ratio:1/1; object-fit:cover; display:block;
    border-radius:1.5rem; border:2px solid rgba(245,197,66,.25);
    background:#1e222a; cursor:pointer;
    transition: transform .2s, border-color .2s;
    box-shadow: 0 10px 20px -10px rgba(0,0,0,.8);
  }
  .gallery img:hover { transform:scale(1.02); border-color:#f5c542; }
  .contact {
    background:linear-gradient(145deg,#141a22,#0f131a);
    border-radius:2rem; padding:1.5rem;
    display:flex; flex-wrap:wrap; justify-content:space-between; align-items:center;
    gap:1rem; border:1px solid rgba(245,197,66,.2); margin-top:1rem;
  }
  .contact-items { display:flex; flex-wrap:wrap; gap:.8rem 1.2rem; }
  .contact-items span {
    display:flex; align-items:center; gap:8px; font-size:.95rem;
    background:rgba(255,255,255,.03); padding:.5rem 1rem; border-radius:3rem;
    border:1px solid rgba(245,197,66,.15);
  }
  .contact-items i { color:#f5c542; }
  .call-btn {
    background:#f5c542; color:#0b0d10; font-weight:600;
    padding:.8rem 1.8rem; border-radius:3rem; text-decoration:none;
    display:inline-flex; align-items:center; gap:8px; font-size:1.05rem;
    box-shadow: 0 10px 18px -8px rgba(245,197,66,.5);
  }
  .call-btn i { color:#0b0d10; }
  footer { text-align:center; margin-top:2rem; padding-top:1.3rem;
           border-top:1px solid rgba(255,255,255,.05);
           color:#7e8a9a; font-size:.85rem; }
  footer i { color:#f5c542; margin-right:6px; }
  .lightbox {
    display:none; position:fixed; inset:0; background:rgba(5,7,10,.94);
    z-index:9999; justify-content:center; align-items:center; padding:1.5rem;
    cursor:zoom-out;
  }
  .lightbox.on { display:flex; }
  .lightbox img { max-width:95vw; max-height:90vh; border-radius:1.5rem; border:2px solid rgba(245,197,66,.3); }
  @media(max-width:600px){
    .page { padding:1.5rem 1rem; border-radius:2rem; }
    header { flex-direction:column; text-align:center; }
    .profile-pic { width:110px; height:110px; }
    h1 { font-size:2rem; }
    .tagline, .details { justify-content:center; }
    h2 { font-size:1.4rem; margin:1.5rem 0 .8rem; }
    .gallery { grid-template-columns:repeat(2,1fr); gap:.7rem; }
    .gallery img { border-radius:1.2rem; }
    .contact { flex-direction:column; text-align:center; }
  }
</style>
</head>
<body>
<div class="page">

  <!-- PROFILE HEADER — uses first image -->
  <header>
    <img class="profile-pic" src="IMG-20261002-WA0005.jpg" alt="Muddasani Rajkumar">
    <div>
      <h1>Muddasani Rajkumar</h1>
      <div class="tagline"><i class="fas fa-film"></i> Artist / Assistant Director</div>
      <div class="details">
        <span><i class="fas fa-calendar-alt"></i> Age: 26</span>
        <span><i class="fas fa-ruler-vertical"></i> Height: 6'5"</span>
        <span><i class="fas fa-map-pin"></i> Hyderabad</span>
        <span><i class="fas fa-phone-alt"></i> 9391271361</span>
      </div>
    </div>
  </header>

  <!-- ABOUT -->
  <h2><i class="fas fa-user-circle"></i> About</h2>
  <div class="about">
    <p><i class="fas fa-quote-left"></i> I am very passionate about acting and assistant directing. When I saw the movie <strong>"Emayachesave"</strong> with Samantha and Chaithanya sir, it deeply inspired me. I started working with small content on TikTok from 2019–2021, where I had good reach with acting videos. I also taught my sister's son acting — how to perform in the real world and in front of the camera.</p>
    <p><i class="fas fa-heart"></i> I am passionate about acting and assistant direction. I definitely believe that I will get an opportunity from you. Thank you.</p>
  </div>

  <!-- GALLERY — exactly 6 images, all your real filenames -->
  <h2><i class="fas fa-images"></i> Gallery</h2>
  <div class="gallery">
    <img src="IMG-20261002-WA0005.jpg" alt="Photo 1" onclick="zoom(this.src)">
    <img src="IMG-20261002-WA0006.jpg" alt="Photo 2" onclick="zoom(this.src)">
    <img src="IMG-20261002-WA0007.jpg" alt="Photo 3" onclick="zoom(this.src)">
    <img src="IMG-20261002-WA0008.jpg" alt="Photo 4" onclick="zoom(this.src)">
    <img src="IMG-20261002-WA0009.jpg" alt="Photo 5" onclick="zoom(this.src)">
    <img src="IMG-20261002-WA0010.jpg" alt="Photo 6" onclick="zoom(this.src)">
  </div>

  <!-- REACH OUT -->
  <h2><i class="fas fa-paper-plane"></i> Reach Out</h2>
  <div class="contact">
    <div class="contact-items">
      <span><i class="fas fa-user"></i> Muddasani Rajkumar</span>
      <span><i class="fas fa-map-marker-alt"></i> Hyderabad</span>
      <span><i class="fas fa-ruler-vertical"></i> 6'5"</span>
      <span><i class="fas fa-cake-candles"></i> 26 yrs</span>
    </div>
    <a href="tel:+919391271361" class="call-btn"><i class="fas fa-phone-alt"></i> 9391271361</a>
  </div>

  <footer>
    <i class="fas fa-star"></i> Muddasani Rajkumar · Actor & Assistant Director · Hyderabad
  </footer>
</div>

<!-- Lightbox -->
<div class="lightbox" id="lb" onclick="this.classList.remove('on')">
  <img id="lb-img" src="" alt="">
</div>

<script>
  function zoom(src){
    document.getElementById('lb-img').src = src;
    document.getElementById('lb').classList.add('on');
  }
  document.addEventListener('keydown', e => { if(e.key==='Escape') document.getElementById('lb').classList.remove('on'); });
</script>
</body>
</html>
