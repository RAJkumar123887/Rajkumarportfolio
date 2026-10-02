<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <meta name="theme-color" content="#0b0d10">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="apple-mobile-web-app-title" content="Rajkumar">
  <title>Muddasani Rajkumar · Actor & Assistant Director</title>
  
  <!-- Preconnect and fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300..700&display=swap" rel="stylesheet">
  
  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  
  <style>
    /* ----- RESET & BASE (iOS-friendly) ----- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      -webkit-text-size-adjust: 100%;
      -webkit-tap-highlight-color: transparent;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
      background: #0b0d10;
      color: #eef2f6;
      line-height: 1.5;
      min-height: 100vh;
      padding: env(safe-area-inset-top) env(safe-area-inset-right) env(safe-area-inset-bottom) env(safe-area-inset-left);
      display: flex;
      align-items: center;
      justify-content: center;
      background-image: radial-gradient(circle at 20% 20%, rgba(245, 197, 66, 0.03) 0%, transparent 40%),
                        radial-gradient(circle at 80% 70%, rgba(245, 197, 66, 0.02) 0%, transparent 50%);
    }

    .page {
      max-width: 1000px;
      width: 100%;
      margin: 1.5rem auto;
      padding: 2.2rem 1.8rem;
      background: rgba(18, 22, 28, 0.92);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-radius: 2.8rem;
      box-shadow: 0 30px 50px -20px rgba(0, 0, 0, 0.9), 0 0 0 1px rgba(245, 197, 66, 0.08);
      border: 1px solid rgba(255, 255, 255, 0.03);
      transition: all 0.2s;
    }

    /* ----- iOS-like smooth interactions ----- */
    a, button, .gallery-item, .reachout-card {
      -webkit-tap-highlight-color: transparent;
      transition: transform 0.15s ease, opacity 0.15s ease, background 0.2s;
    }

    a:active, button:active, .gallery-item:active {
      opacity: 0.7;
      transform: scale(0.98);
    }

    /* ----- HEADER (photo + name) ----- */
    .portfolio-header {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 1.8rem;
      margin-bottom: 2rem;
      padding-bottom: 1.6rem;
      border-bottom: 1.5px solid rgba(245, 197, 66, 0.2);
    }

    .header-photo {
      flex-shrink: 0;
    }

    .header-photo img {
      width: 130px;
      height: 130px;
      object-fit: cover;
      border-radius: 50%;
      border: 3.5px solid #f5c542;
      box-shadow: 0 12px 24px -8px rgba(245, 197, 66, 0.25);
      background: #1e222a;
      display: block;
      transition: border-color 0.2s;
    }

    .header-photo img:hover {
      border-color: #ffd95e;
    }

    .header-text h1 {
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      line-height: 1.1;
      background: linear-gradient(to right, #ffffff, #f5e6b0);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 0.2rem;
    }

    .header-text .tagline {
      font-size: 1.2rem;
      font-weight: 400;
      color: #b0b8c5;
      margin-bottom: 0.8rem;
      letter-spacing: 0.3px;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .header-text .tagline i {
      color: #f5c542;
      font-size: 1.1rem;
    }

    .header-details {
      display: flex;
      flex-wrap: wrap;
      gap: 1.4rem 2rem;
      color: #cbd5e1;
      font-size: 1rem;
      margin-top: 0.3rem;
    }

    .header-details span {
      display: flex;
      align-items: center;
      gap: 8px;
      white-space: nowrap;
    }

    .header-details i {
      color: #f5c542;
      width: 18px;
      text-align: center;
      font-size: 1rem;
    }

    /* ----- SECTION TITLES ----- */
    .section-title {
      font-size: 1.9rem;
      font-weight: 600;
      margin: 2.2rem 0 1.2rem 0;
      display: flex;
      align-items: center;
      gap: 12px;
      color: #ffffff;
      letter-spacing: -0.01em;
    }

    .section-title i {
      color: #f5c542;
      font-size: 1.7rem;
      width: 32px;
    }

    .section-title::after {
      content: '';
      flex: 1;
      height: 1.5px;
      background: linear-gradient(to right, #f5c542, transparent);
      margin-left: 8px;
      border-radius: 2px;
    }

    /* ----- ABOUT ----- */
    .about-text {
      background: rgba(30, 35, 45, 0.7);
      padding: 1.8rem 1.8rem;
      border-radius: 2rem;
      border-left: 5px solid #f5c542;
      font-size: 1.05rem;
      color: #d6dee8;
      box-shadow: 0 8px 18px -6px rgba(0, 0, 0, 0.5);
      backdrop-filter: blur(4px);
      -webkit-backdrop-filter: blur(4px);
    }

    .about-text p {
      margin-bottom: 1rem;
    }

    .about-text p:last-child {
      margin-bottom: 0;
    }

    .about-text i {
      color: #f5c542;
      margin-right: 6px;
      font-size: 0.95rem;
    }

    .about-text strong {
      color: #f5e6b0;
      font-weight: 600;
    }

    /* ----- GALLERY (4-5 photos) ----- */
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 1rem;
      margin: 0.5rem 0 0.5rem;
    }

    .gallery-item {
      aspect-ratio: 1 / 1;
      border-radius: 1.8rem;
      overflow: hidden;
      background: #1e222a;
      border: 2px solid rgba(245, 197, 66, 0.25);
      transition: transform 0.2s ease, border-color 0.2s ease, box-shadow 0.2s ease;
      box-shadow: 0 10px 20px -10px rgba(0, 0, 0, 0.8);
      will-change: transform;
    }

    .gallery-item:hover {
      transform: scale(1.02);
      border-color: #f5c542;
      box-shadow: 0 16px 28px -10px rgba(245, 197, 66, 0.3);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    /* ----- REACH OUT ----- */
    .reachout-card {
      background: linear-gradient(145deg, #141a22, #0f131a);
      border-radius: 2.2rem;
      padding: 1.8rem 2rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      border: 1px solid rgba(245, 197, 66, 0.2);
      box-shadow: 0 18px 32px -12px #000000;
      margin-top: 1.2rem;
      gap: 1.2rem;
      backdrop-filter: blur(4px);
      -webkit-backdrop-filter: blur(4px);
    }

    .reachout-details {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem 2rem;
    }

    .reachout-item {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 1.05rem;
      background: rgba(255, 255, 255, 0.03);
      padding: 0.5rem 1.2rem;
      border-radius: 3rem;
      border: 1px solid rgba(245, 197, 66, 0.15);
      white-space: nowrap;
    }

    .reachout-item i {
      color: #f5c542;
      font-size: 1.2rem;
      width: 24px;
      text-align: center;
    }

    .contact-highlight {
      background: #f5c542;
      color: #0b0d10;
      font-weight: 600;
      padding: 0.9rem 2rem;
      border-radius: 3rem;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-size: 1.15rem;
      letter-spacing: 0.3px;
      border: none;
      transition: background 0.2s, transform 0.15s, box-shadow 0.2s;
      text-decoration: none;
      box-shadow: 0 10px 18px -8px #f5c54260;
      white-space: nowrap;
    }

    .contact-highlight i {
      color: #0b0d10;
      font-size: 1.25rem;
    }

    .contact-highlight:hover {
      background: #ffd95e;
      transform: translateY(-2px);
      box-shadow: 0 16px 26px -8px #f5c54290;
    }

    .contact-highlight:active {
      transform: scale(0.97);
      opacity: 0.9;
    }

    /* ----- FOOTER ----- */
    .footer-note {
      text-align: center;
      margin-top: 2.2rem;
      font-size: 0.88rem;
      color: #7e8a9a;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
      padding-top: 1.6rem;
      letter-spacing: 0.2px;
    }

    .footer-note i {
      color: #f5c542;
      margin-right: 6px;
    }

    /* ----- RESPONSIVE (iOS optimized) ----- */
    @media (max-width: 700px) {
      body {
        padding: 0.8rem;
        align-items: flex-start;
      }
      .page {
        padding: 1.8rem 1.2rem;
        border-radius: 2.2rem;
        margin: 0.5rem auto;
      }
      .portfolio-header {
        flex-direction: column;
        text-align: center;
        gap: 1rem;
        padding-bottom: 1.4rem;
      }
      .header-photo img {
        width: 120px;
        height: 120px;
      }
      .header-text h1 {
        font-size: 2.2rem;
      }
      .header-text .tagline {
        justify-content: center;
        font-size: 1.1rem;
      }
      .header-details {
        justify-content: center;
        gap: 1rem 1.5rem;
        font-size: 0.95rem;
      }
      .section-title {
        font-size: 1.7rem;
        margin: 1.8rem 0 1rem 0;
      }
      .section-title i {
        font-size: 1.5rem;
        width: 28px;
      }
      .about-text {
        padding: 1.4rem 1.2rem;
        font-size: 1rem;
        border-left-width: 4px;
        border-radius: 1.6rem;
      }
      .gallery-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 0.8rem;
      }
      .gallery-item {
        border-radius: 1.4rem;
      }
      .reachout-card {
        flex-direction: column;
        text-align: center;
        padding: 1.6rem 1.2rem;
        border-radius: 1.8rem;
      }
      .reachout-details {
        justify-content: center;
        gap: 0.8rem 1.2rem;
      }
      .reachout-item {
        font-size: 0.95rem;
        padding: 0.4rem 1rem;
      }
      .contact-highlight {
        font-size: 1.1rem;
        padding: 0.8rem 2rem;
      }
      .footer-note {
        font-size: 0.8rem;
        margin-top: 1.8rem;
        padding-top: 1.2rem;
      }
    }

    @media (max-width: 380px) {
      .page {
        padding: 1.4rem 1rem;
      }
      .header-text h1 {
        font-size: 1.9rem;
      }
      .header-details span {
        font-size: 0.85rem;
      }
      .gallery-grid {
        grid-template-columns: 1fr 1fr;
        gap: 0.6rem;
      }
      .reachout-details {
        flex-direction: column;
        align-items: center;
        gap: 0.6rem;
      }
    }

    /* iPhone notch / dynamic island safe area */
    @supports (padding: max(0px)) {
      body {
        padding-left: max(0.8rem, env(safe-area-inset-left));
        padding-right: max(0.8rem, env(safe-area-inset-right));
        padding-top: max(0.8rem, env(safe-area-inset-top));
        padding-bottom: max(0.8rem, env(safe-area-inset-bottom));
      }
    }

    /* Smooth focus for accessibility */
    a:focus-visible, button:focus-visible {
      outline: 2px solid #f5c542;
      outline-offset: 4px;
      border-radius: 4px;
    }

    /* Placeholder fallback style */
    .img-placeholder {
      background: #252b35;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #f5c542;
      font-size: 2rem;
      font-weight: 300;
    }
  </style>
</head>
<body>
  <div class="page">
    <!-- ========== HEADER ========== -->
    <header class="portfolio-header">
      <div class="header-photo">
        <!-- Replace with your actual photo (portrait works best) -->
        <img 
          src="https://placehold.co/400x400/1e222a/f5c542?text=Rajkumar+Photo" 
          alt="Muddasani Rajkumar portrait" 
          loading="eager"
        >
      </div>
      <div class="header-text">
        <h1>Muddasani Rajkumar</h1>
        <div class="tagline">
          <i class="fas fa-film"></i> Artist / Assistant Director
        </div>
        <div class="header-details">
          <span><i class="fas fa-calendar-alt"></i> Age: 26</span>
          <span><i class="fas fa-ruler-vertical"></i> Height: 6'5"</span>
          <span><i class="fas fa-map-pin"></i> Hyderabad</span>
          <span><i class="fas fa-phone-alt"></i> 9391271361</span>
        </div>
      </div>
    </header>

    <!-- ========== ABOUT ========== -->
    <h2 class="section-title"><i class="fas fa-user-circle"></i> About</h2>
    <div class="about-text">
      <p>
        <i class="fas fa-quote-left"></i> 
        I am very passionate about acting and assistant directing. When I saw the movie 
        <strong>“Emayachesave”</strong> with Samantha and Chaithanya sir, it deeply inspired me. 
        I started working with small content on TikTok from 2019–2021, where I had good reach 
        with acting videos. I also taught my sister’s son acting — how to perform in the real world 
        and in front of the camera.
      </p>
      <p>
        <i class="fas fa-heart"></i> 
        I am passionate about acting and assistant direction. I definitely believe that I will get 
        an opportunity from you. Thank you.
      </p>
    </div>

    <!-- ========== GALLERY (4-5 photos) ========== -->
    <h2 class="section-title"><i class="fas fa-images"></i> Gallery</h2>
    <div class="gallery-grid">
      <!-- Replace each src with your own photos (square works best) -->
      <div class="gallery-item">
        <img src="https://placehold.co/600x600/1e222a/f5c542?text=Photo+1" alt="Portfolio photo 1" loading="lazy">
      </div>
      <div class="gallery-item">
        <img src="https://placehold.co/600x600/1e222a/f5c542?text=Photo+2" alt="Portfolio photo 2" loading="lazy">
      </div>
      <div class="gallery-item">
        <img src="https://placehold.co/600x600/1e222a/f5c542?text=Photo+3" alt="Portfolio photo 3" loading="lazy">
      </div>
      <div class="gallery-item">
        <img src="https://placehold.co/600x600/1e222a/f5c542?text=Photo+4" alt="Portfolio photo 4" loading="lazy">
      </div>
      <div class="gallery-item">
        <img src="https://placehold.co/600x600/1e222a/f5c542?text=Photo+5" alt="Portfolio photo 5" loading="lazy">
      </div>
    </div>

    <!-- ========== REACH OUT ========== -->
    <h2 class="section-title"><i class="fas fa-paper-plane"></i> Reach Out</h2>
    <div class="reachout-card">
      <div class="reachout-details">
        <div class="reachout-item">
          <i class="fas fa-user"></i> Muddasani Rajkumar
        </div>
        <div class="reachout-item">
          <i class="fas fa-map-marker-alt"></i> Hyderabad
        </div>
        <div class="reachout-item">
          <i class="fas fa-ruler-vertical"></i> 6'5"
        </div>
        <div class="reachout-item">
          <i class="fas fa-cake-candles"></i> 26 yrs
        </div>
      </div>
      <a href="tel:+919391271361" class="contact-highlight" aria-label="Call Muddasani Rajkumar">
        <i class="fas fa-phone-alt"></i> 9391271361
      </a>
    </div>

    <!-- ========== FOOTER ========== -->
    <div class="footer-note">
      <i class="fas fa-star"></i>
      Muddasani Rajkumar · Actor & Assistant Director · Hyderabad
    </div>
  </div>
</body>
</html>
