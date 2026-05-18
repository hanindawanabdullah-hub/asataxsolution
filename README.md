<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ASA TAX SOLUTION</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
    }

    :root{
      --primary:#e84e1b;
      --secondary:#ff6b2c;
      --light:#fff7f4;
      --text:#2d2d2d;
      --gray:#6b6b6b;
      --border:#ececec;
      --shadow:0 10px 30px rgba(0,0,0,.08);
    }

    body{
      font-family:'Poppins',sans-serif;
      background:white;
      color:var(--text);
      overflow-x:hidden;
    }

    .container{
      width:90%;
      max-width:1250px;
      margin:auto;
    }

    /* NAVBAR */

    nav{
      position:fixed;
      top:0;
      width:100%;
      background:rgba(255,255,255,.95);
      backdrop-filter:blur(12px);
      border-bottom:1px solid var(--border);
      z-index:999;
    }

    .navbar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:16px 0;
    }

    .navbar img{
      height:62px;
    }

    .menu{
      display:flex;
      gap:35px;
      align-items:center;
    }

    .menu a{
      text-decoration:none;
      color:var(--text);
      font-size:15px;
      font-weight:500;
      transition:.3s;
    }

    .menu a:hover{
      color:var(--primary);
    }

    /* SECTION */

    section{
      padding:110px 0;
    }

    /* HERO */

    .hero{
      padding-top:180px;
      background:
      radial-gradient(circle at top right, #fff0ea 0%, transparent 35%);
    }

    .hero-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:70px;
      align-items:center;
    }

    .hero h1{
      font-size:68px;
      line-height:1.08;
      margin-bottom:28px;
      font-weight:800;
      color:#111;
    }

    .highlight{
      color:var(--primary);
    }

    .hero p{
      color:var(--gray);
      line-height:2;
      font-size:17px;
      margin-bottom:35px;
      max-width:600px;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      gap:10px;
      background:linear-gradient(135deg,var(--primary),var(--secondary));
      color:white;
      padding:18px 34px;
      border-radius:16px;
      text-decoration:none;
      font-weight:700;
      box-shadow:0 10px 25px rgba(232,78,27,.2);
      transition:.3s;
    }

    .btn:hover{
      transform:translateY(-3px);
    }

    /* CARD */

    .card{
      background:white;
      border:1px solid var(--border);
      border-radius:28px;
      padding:35px;
      box-shadow:var(--shadow);
    }

    /* FLOATING AI CHAT */

    .floating-chat{
      position:fixed;
      bottom:30px;
      right:30px;
      width:380px;
      z-index:9999;
      animation:fadeIn .5s ease;
    }

    @keyframes fadeIn{
      from{
        opacity:0;
        transform:translateY(20px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    .chat-header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      margin-bottom:20px;
    }

    .chat-header h2{
      color:var(--primary);
      font-size:22px;
    }

    .chat-status{
      background:#e9fff0;
      color:#00a63e;
      font-size:12px;
      padding:6px 12px;
      border-radius:30px;
      font-weight:600;
    }

    .chat-box{
      height:300px;
      overflow-y:auto;
      padding-right:5px;
      margin-bottom:20px;
    }

    .chat{
      padding:16px 18px;
      border-radius:18px;
      margin-bottom:15px;
      line-height:1.8;
      font-size:14px;
    }

    .bot{
      background:#f7f7f7;
      border:1px solid #ededed;
      color:#444;
    }

    .user{
      background:linear-gradient(135deg,var(--primary),var(--secondary));
      color:white;
      margin-left:40px;
    }

    .chat-input{
      display:flex;
      gap:10px;
    }

    .chat-input input{
      flex:1;
      padding:16px;
      border:1px solid #ddd;
      border-radius:14px;
      outline:none;
      font-family:'Poppins',sans-serif;
      font-size:14px;
    }

    .chat-input input:focus{
      border-color:var(--primary);
    }

    .chat-input button{
      background:linear-gradient(135deg,var(--primary),var(--secondary));
      border:none;
      color:white;
      padding:16px 22px;
      border-radius:14px;
      font-weight:700;
      cursor:pointer;
    }

    /* TITLE */

    .title{
      font-size:50px;
      text-align:center;
      margin-bottom:70px;
      font-weight:800;
      color:#111;
    }

    /* ABOUT */

    .about-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:60px;
      align-items:start;
    }

    .about p{
      color:var(--gray);
      line-height:2;
      margin-bottom:20px;
    }

    .vision-card{
      margin-bottom:25px;
    }

    .vision-card h3{
      color:var(--primary);
      margin-bottom:15px;
      font-size:24px;
    }

    .culture-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:15px;
      margin-top:20px;
    }

    .culture{
      background:var(--light);
      border:1px solid #ffe1d4;
      padding:20px;
      border-radius:20px;
      display:flex;
      gap:15px;
      align-items:flex-start;
    }

    .culture span{
      font-size:26px;
    }

    .culture p{
      margin:0;
      font-size:14px;
      color:#444;
      line-height:1.7;
    }

    /* SERVICES */

    .services-grid,
    .blog-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:25px;
    }

    .service{
      background:white;
      border:1px solid var(--border);
      padding:35px;
      border-radius:26px;
      box-shadow:var(--shadow);
      transition:.3s;
    }

    .service:hover{
      transform:translateY(-6px);
    }

    .service h3{
      margin-bottom:18px;
      font-size:22px;
      color:var(--primary);
    }

    .service p{
      color:var(--gray);
      line-height:1.9;
      font-size:14px;
    }

    /* BLOG */

    .blog{
      background:white;
      border-radius:26px;
      overflow:hidden;
      border:1px solid var(--border);
      box-shadow:var(--shadow);
    }

    .blog-img{
      height:220px;
      background:
      linear-gradient(135deg,#ffefe8,#ffd6c7);
    }

    .blog-content{
      padding:28px;
    }

    .blog h3{
      margin-bottom:15px;
      color:#111;
    }

    .blog p{
      color:var(--gray);
      line-height:1.9;
      margin-bottom:22px;
      font-size:14px;
    }

    .read-btn{
      background:linear-gradient(135deg,var(--primary),var(--secondary));
      color:white;
      padding:12px 20px;
      border:none;
      border-radius:12px;
      font-weight:700;
      cursor:pointer;
    }

    /* MODAL */

    .modal{
      position:fixed;
      inset:0;
      background:rgba(0,0,0,.7);
      display:none;
      justify-content:center;
      align-items:center;
      z-index:99999;
      padding:30px;
    }

    .modal-content{
      background:white;
      max-width:800px;
      width:100%;
      padding:40px;
      border-radius:30px;
      max-height:90vh;
      overflow-y:auto;
      box-shadow:0 20px 60px rgba(0,0,0,.2);
    }

    .close{
      float:right;
      cursor:pointer;
      font-size:30px;
      color:var(--primary);
    }

    /* CONTACT */

    .contact{
      text-align:center;
      background:linear-gradient(135deg,#fff7f4,#fff);
    }

    .contact p{
      margin:15px 0;
      color:#555;
      font-size:16px;
    }

    footer{
      text-align:center;
      padding:30px;
      border-top:1px solid var(--border);
      color:#777;
      font-size:14px;
    }

    /* MOBILE */

    @media(max-width:1000px){

      .hero-grid,
      .about-grid,
      .services-grid,
      .blog-grid{
        grid-template-columns:1fr;
      }

      .hero h1{
        font-size:48px;
      }

      .menu{
        display:none;
      }

      .floating-chat{
        width:92%;
        right:4%;
        bottom:20px;
      }

    }

  </style>
</head>

<body>

<!-- NAVBAR -->

<nav>
  <div class="container navbar">

    <img src="logo.png" alt="ASA TAX">

    <div class="menu">
      <a href="#home">Beranda</a>
      <a href="#about">Tentang Kami</a>
      <a href="#services">Layanan</a>
      <a href="#blog">Artikel</a>
      <a href="#contact">Kontak</a>
    </div>

  </div>
</nav>

<!-- HERO -->

<section class="hero" id="home">

  <div class="container hero-grid">

    <div>

      <h1>
        SOLUSI <span class="highlight">PERPAJAKAN</span><br>
        PROFESIONAL<br>
        UNTUK BISNIS ANDA
      </h1>

      <p>
        ASA TAX SOLUTION adalah konsultan pajak profesional terpercaya
        dengan pengalaman lebih dari 20 tahun dalam bidang perpajakan
        dan akuntansi perusahaan.
      </p>

      <a href="https://wa.me/6282136961885" class="btn">
        Konsultasi Sekarang
      </a>

    </div>

    <div class="card">

      <h2 style="font-size:34px; margin-bottom:20px;">
        Konsultan Pajak Modern & Profesional
      </h2>

      <p style="color:#666; line-height:2;">
        Membantu perusahaan dalam pengelolaan perpajakan,
        tax planning, review pajak, dan pendampingan pemeriksaan
        secara profesional dan terpercaya.
      </p>

    </div>

  </div>

</section>

<!-- ABOUT -->

<section id="about">

  <div class="container about-grid">

    <div class="about">

      <h2 class="title" style="text-align:left;">
        Tentang <span class="highlight">Kami</span>
      </h2>

      <p>
        CV Asa Tax Solution adalah perusahaan Konsultan Pajak dan Akuntansi
        yang berlokasi di Kartasura, Sukoharjo, dan telah berdiri sejak 7 Januari 2005.
      </p>

      <p>
        Dengan pengalaman dan keahlian yang dimiliki, CV Asa Tax Solution
        hadir sebagai mitra terpercaya untuk membantu perusahaan mengelola
        aspek keuangan dan perpajakan secara profesional.
      </p>

    </div>

    <div>

      <div class="card vision-card">

        <h3>VISI</h3>

        <p>
          Menjadi konsultan pajak yang profesional,
          terpercaya dan handal.
        </p>

      </div>

      <div class="card vision-card">

        <h3>MISI</h3>

        <p>
          Memberi edukasi, solusi, dan berkomitmen
          dalam pelayanan perpajakan.
        </p>

      </div>

      <div class="card">

        <h3 class="highlight">Budaya Kerja</h3>

        <div class="culture-grid">

          <div class="culture">
            <span>🕌</span>
            <p>Basmallah & Hamdallah</p>
          </div>

          <div class="culture">
            <span>📊</span>
            <p>Disiplin Kerja</p>
          </div>

          <div class="culture">
            <span>😊</span>
            <p>Ramah & Smart</p>
          </div>

          <div class="culture">
            <span>🤝</span>
            <p>Kerjasama Tim</p>
          </div>

          <div class="culture">
            <span>⚡</span>
            <p>Cepat Tanggap</p>
          </div>

          <div class="culture">
            <span>🔒</span>
            <p>Kerahasiaan Klien</p>
          </div>

        </div>

      </div>

    </div>

  </div>

</section>

<!-- SERVICES -->

<section id="services">

  <div class="container">

    <h2 class="title">
      Layanan <span class="highlight">Kami</span>
    </h2>

    <div class="services-grid">

      <div class="service">

        <h3>Konsultasi Perpajakan</h3>

        <p>
          Memberikan solusi perpajakan profesional sesuai regulasi Indonesia.
        </p>

      </div>

      <div class="service">

        <h3>Review Pajak</h3>

        <p>
          Memastikan laporan dan dokumen pajak sesuai ketentuan.
        </p>

      </div>

      <div class="service">

        <h3>Tax Planning</h3>

        <p>
          Perencanaan pajak legal untuk efisiensi perusahaan.
        </p>

      </div>

    </div>

  </div>

</section>

<!-- BLOG -->

<section id="blog">

  <div class="container">

    <h2 class="title">
      Artikel <span class="highlight">Perpajakan</span>
    </h2>

    <div class="blog-grid">

      <div class="blog">

        <div class="blog-img"></div>

        <div class="blog-content">

          <h3>Strategi Efisiensi Pajak</h3>

          <p>
            Strategi legal untuk efisiensi pajak perusahaan.
          </p>

          <button class="read-btn" onclick="openBlog(
            'Strategi Efisiensi Pajak',
            'Efisiensi pajak perusahaan dilakukan melalui tax planning legal dan kepatuhan perpajakan yang baik.'
          )">
            Baca Selengkapnya
          </button>

        </div>

      </div>

      <div class="blog">

        <div class="blog-img"></div>

        <div class="blog-content">

          <h3>Cara Menghadapi SP2DK</h3>

          <p>
            Panduan menghadapi SP2DK dari DJP.
          </p>

          <button class="read-btn" onclick="openBlog(
            'Cara Menghadapi SP2DK',
            'SP2DK merupakan surat dari DJP yang memerlukan klarifikasi data perpajakan.'
          )">
            Baca Selengkapnya
          </button>

        </div>

      </div>

    </div>

  </div>

</section>

<!-- CONTACT -->

<section id="contact">

  <div class="container card contact">

    <h2 class="title">
      Hubungi <span class="highlight">Kami</span>
    </h2>

    <p>(0271) 7451358</p>
    <p>+62 821-3696-1885</p>
    <p>asataxs@gmail.com</p>
    <p>Jalan Perkutut No.17-A, Gonilan, Kartasura, Sukoharjo</p>

  </div>

</section>

<!-- FLOATING CHATBOT -->

<div class="floating-chat">

  <div class="card">

    <div class="chat-header">

      <h2>ASA CHATBOT AI</h2>

      <div class="chat-status">
        Online
      </div>

    </div>

    <div class="chat-box" id="chatBox">

      <div class="chat bot">
        Halo 👋 Saya ASA CHATBOT AI.
        Silakan tanyakan seputar pajak,
        NPWP, PPN, SP2DK, dan layanan ASA TAX Solution.
      </div>

    </div>

    <div class="chat-input">

      <input type="text" id="message" placeholder="Tanyakan sesuatu...">

      <button onclick="sendChat()">
        Kirim
      </button>

    </div>

  </div>

</div>

<!-- MODAL -->

<div class="modal" id="modal">

  <div class="modal-content">

    <span class="close" onclick="closeModal()">✕</span>

    <h2 id="modalTitle" class="highlight"></h2>

    <p id="modalContent" style="margin-top:20px; line-height:2;"></p>

  </div>

</div>

<footer>
  © 2026 ASA TAX SOLUTION — Professional Tax Consultant
</footer>

<script>

function sendChat(){

  let input = document.getElementById("message");
  let message = input.value.toLowerCase();

  if(message.trim() === "") return;

  let chatBox = document.getElementById("chatBox");

  chatBox.innerHTML += `
    <div class="chat user">
      ${message}
    </div>
  `;

  let reply = "Tim ASA TAX Solution siap membantu kebutuhan perpajakan anda.";

  if(message.includes("npwp")){
    reply = "Pengurusan NPWP memerlukan dokumen legalitas usaha dan identitas direktur.";
  }

  else if(message.includes("ppn")){
    reply = "PPN adalah Pajak Pertambahan Nilai yang dikenakan pada transaksi barang dan jasa.";
  }

  else if(message.includes("sp2dk")){
    reply = "SP2DK adalah surat permintaan klarifikasi data perpajakan dari DJP.";
  }

  else if(message.includes("restitusi")){
    reply = "Restitusi pajak adalah pengembalian kelebihan pembayaran pajak.";
  }

  setTimeout(() => {

    chatBox.innerHTML += `
      <div class="chat bot">
        ${reply}
        <br><br>
        Untuk konsultasi lebih lanjut silakan hubungi WhatsApp:
        <br>
        <b>+62 821-3696-1885</b>
      </div>
    `;

    chatBox.scrollTop = chatBox.scrollHeight;

  },500);

  input.value = "";

}

function openBlog(title,content){

  document.getElementById("modal").style.display = "flex";
  document.getElementById("modalTitle").innerText = title;
  document.getElementById("modalContent").innerText = content;

}

function closeModal(){

  document.getElementById("modal").style.display = "none";

}

</script>

</body>
</html>
