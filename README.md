<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>DRAKEN SHOP</title>
<style>
  html {
    scroll-behavior: smooth;
  }
  body {
    font-family: Arial, sans-serif;
    margin: 0; padding: 0;
    color: white;
    overflow-x: hidden;
    background: linear-gradient(135deg, #ff00cc, #3333ff, #00ffcc, #ff6600);
    background-size: 400% 400%;
    animation: gradientBG 12s ease infinite;
  }
  body::before {
    content: "";
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: transparent url('https://www.transparenttextures.com/patterns/stardust.png') repeat;
    z-index: -1;
    animation: starsMove 60s linear infinite;
    opacity: 0.3;
  }
  @keyframes starsMove {
    from { background-position: 0 0; }
    to { background-position: -10000px 5000px; }
  }
  @keyframes gradientBG {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
  }
  header {
    background: rgba(0, 0, 0, 0.6);
    padding: 15px 0;
    text-align: center;
    position: sticky;
    top: 0;
    z-index: 100;
    backdrop-filter: blur(8px);
  }
  header nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    gap: 20px;
  }
  header nav a {
    color: white;
    text-decoration: none;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;
  }
  header nav a:hover {
    color: yellow;
  }
  main {
    max-width: 1000px;
    margin: 20px auto;
    overflow: hidden;
    position: relative;
  }
  section {
    position: relative;
    opacity: 0;
    height: 0;
    overflow: hidden;
    transition: opacity 0.5s ease, height 0.5s ease;
  }
  section.active {
    opacity: 1;
    height: auto;
    overflow: visible;
  }
  h1, h2 {
    text-align: center;
    text-shadow: 0 0 10px #fff, 0 0 20px #ff00cc, 0 0 30px #00ffcc;
  }
  .produk ul {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 0;
    list-style: none;
  }
  .produk li {
    background: rgba(255, 255, 255, 0.08);
    border-radius: 15px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 0 25px rgba(0,0,0,0.5), 0 0 10px #ff00cc;
    backdrop-filter: blur(10px);
    cursor: pointer;
    transition: transform 0.3s, box-shadow 0.3s;
  }
  .produk li:hover {
    transform: scale(1.05);
    box-shadow: 0 0 35px rgba(255,255,255,0.6), 0 0 20px #00ffcc;
  }
  .produk img {
    width: 150px;
    height: 150px;
    object-fit: cover;
    border-radius: 50%;
    border: 3px solid white;
    margin-bottom: 10px;
  }
  .btn-beli {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin-top: 10px;
  }
  .btn-beli a {
    background: linear-gradient(90deg, #ff00cc, #3333ff);
    padding: 8px 12px;
    border-radius: 5px;
    color: white;
    text-decoration: none;
    font-size: 14px;
    transition: 0.3s;
  }
  .btn-beli a:hover {
    background: linear-gradient(90deg, #00ffcc, #ff00cc);
    transform: scale(1.05);
  }
  #kontak {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 25px;
    font-size: 1.2rem;
  }
  #kontak h2 {
    font-size: 2.5rem;
    margin-bottom: 0;
    text-shadow: 0 0 15px #fff, 0 0 25px #ff00cc, 0 0 35px #00ffcc;
  }
  #kontak .btn-kontak {
    display: flex;
    gap: 20px;
  }
  #kontak .btn-kontak a {
    background: linear-gradient(90deg, #ff00cc, #3333ff);
    padding: 15px 25px;
    border-radius: 10px;
    color: white;
    text-decoration: none;
    font-size: 1.2rem;
    font-weight: bold;
    transition: 0.3s;
    box-shadow: 0 0 15px #ff00cc;
  }
  #kontak .btn-kontak a:hover {
    background: linear-gradient(90deg, #00ffcc, #ff00cc);
    transform: scale(1.05);
    box-shadow: 0 0 25px #00ffcc;
  }
  footer {
    text-align: center;
    padding: 15px;
    background: rgba(0,0,0,0.6);
    margin-top: 20px;
  }
</style>
</head>
<body>
<header>
  <nav>
    <ul>
      <li><a onclick="showSection('beranda')">Beranda</a></li>
      <li><a onclick="showSection('produk')">Produk</a></li>
      <li><a onclick="showSection('kontak')">Kontak</a></li>
    </ul>
  </nav>
</header>

<main>
  <section id="beranda" class="active">
    <h1>Selamat Datang di Draken Shop!</h1>
    <p style="text-align:center;">Kami menyediakan berbagai produk pilihan untuk Anda.</p>
  </section>

  <section class="produk" id="produk">
    <h2>Produk Kami</h2>
    <ul>
      <li>
        <img src="https://files.catbox.moe/0458zj.jpg" alt="MURBAND" />
        <h3>MURBAND</h3>
        <p>Harga: Rp 65.000</p>
        <div class="btn-beli">
          <a href="https://t.me/kalananakbaik" target="_blank">Beli via Telegram</a>
          <a href="https://wa.me/628388666362" target="_blank">Beli via WhatsApp</a>
        </div>
      </li>
      <li>
        <img src="https://files.catbox.moe/yg4xjt.jpg" alt="JASA BAND ALL SOSMED" />
        <h3>JASA BAND ALL SOSMED</h3>
        <p>Harga: Rp 20.000</p>
        <div class="btn-beli">
          <a href="https://kalananakbaik" target="_blank">Beli via Telegram</a>
          <a href="https://wa.me/628388666362" target="_blank">Beli via WhatsApp</a>
        </div>
      </li>
    </ul>
  </section>

<footer>
  <p>&copy; 2025 Draken Shop. All rights reserved.</p>
</footer>

  <section id="kontak">
    <h2>Hubungi Kami</h2>
    <div class="btn-kontak">
      <a href="https://t.me/kalananakbaik" target="_blank">Telegram</a>
      <a href="https://wa.me/628388666362" target="_blank">WhatsApp</a>
    </div>
  </section>
</main>

<script>
  function showSection(id) {
    const sections = document.querySelectorAll('main section');
    sections.forEach(section => {
      if(section.id === id) {
        section.classList.add('active');
      } else {
        section.classList.remove('active');
      }
    });
  }
</script>
</body>
</html>
