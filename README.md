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

    body{
      font-family:'Poppins',sans-serif;
      background:#081B33;
      color:white;
    }

    nav{
      position:fixed;
      top:0;
      width:100%;
      background:rgba(8,27,51,.95);
      backdrop-filter:blur(10px);
      border-bottom:1px solid rgba(255,255,255,.1);
      z-index:999;
    }

    .container{
      width:90%;
      max-width:1300px;
      margin:auto;
    }

    .navbar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:20px 0;
    }

    .navbar img{
      height:70px;
    }

    .menu{
      display:flex;
      gap:30px;
    }

    .menu a{
      text-decoration:none;
      color:#ddd;
      font-size:14px;
      transition:.3s;
    }

    .menu a:hover{
      color:#F5B942;
    }

    section{
      padding:120px 0;
    }

    .hero{
      padding-top:180px;
    }

    .hero-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:60px;
      align-items:center;
    }

    .hero h1{
      font-size:65px;
      line-height:1.1;
      margin-bottom:25px;
      font-weight:800;
    }

    .gold{
      color:#F5B942;
    }

    .hero p{
      color:#cfcfcf;
      line-height:1.9;
      margin-bottom:35px;
      font-size:17px;
    }

    .btn{
      background:#F5B942;
      color:black;
      padding:18px 35px;
      border-radius:15px;
      text-decoration:none;
      font-weight:700;
      display:inline-block;
    }

    .card{
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.1);
      border-radius:30px;
      padding:35px;
    }

    .chat-box{
      height:320px;
      overflow-y:auto;
      margin-bottom:20px;
    }

    .chat{
      padding:15px;
      border-radius:15px;
      margin-bottom:15px;
      line-height:1.7;
      font-size:14px;
    }

    .bot{
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.1);
    }

    .user{
      background:#F5B942;
      color:black;
      margin-left:50px;
    }

    .chat-input{
      display:flex;
      gap:10px;
    }

    .chat-input input{
      flex:1;
      padding:16px;
      border:none;
      border-radius:15px;
      background:rgba(255,255,255,.05);
      color:white;
    }

    .chat-input button{
      background:#F5B942;
      border:none;
      padding:16px 25px;
      border-radius:15px;
      font-weight:700;
      cursor:pointer;
    }

    .title{
      font-size:50px;
      text-align:center;
      margin-bottom:70px;
      font-weight:800;
    }

    .about-grid,
    .hero-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:50px;
    }

    .about p{
      color:#ccc;
      line-height:2;
      margin-bottom:20px;
    }

    .vision-card{
      margin-bottom:25px;
    }

    .vision-card h3{
      color:#F5B942;
      margin-bottom:15px;
      font-size:25px;
    }

    .culture-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:15px;
      margin-top:20px;
    }

    .culture{
      background:rgba(245,185,66,.1);
      border:1px solid rgba(245,185,66,.2);
      padding:20px;
      border-radius:20px;
      display:flex;
      gap:15px;
      align-items:flex-start;
    }

    .culture span{
      font-size:28px;
    }

    .culture p{
      margin:0;
      font-size:13px;
      line-height:1.7;
    }

    .services-grid,
    .blog-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:25px;
    }

    .service{
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.1);
      padding:30px;
      border-radius:25px;
    }

    .service h3{
      margin:20px 0;
      font-size:20px;
    }

    .service p{
      color:#ccc;
      line-height:1.8;
      font-size:14px;
    }

    .blog{
      background:rgba(255,255,255,.05);
      border-radius:25px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,.1);
    }

    .blog-img{
      height:220px;
      background:linear-gradient(135deg,#F5B94233,transparent);
    }

    .blog-content{
      padding:25px;
    }

    .blog h3{
      margin-bottom:15px;
    }

    .blog p{
      color:#ccc;
      line-height:1.8;
      margin-bottom:20px;
      font-size:14px;
    }

    .read-btn{
      background:#F5B942;
      color:black;
      padding:12px 20px;
      border:none;
      border-radius:12px;
      font-weight:700;
      cursor:pointer;
    }

    .modal{
      position:fixed;
      inset:0;
      background:rgba(0,0,0,.8);
      display:none;
      justify-content:center;
      align-items:center;
      z-index:9999;
      padding:30px;
    }

    .modal-content{
      background:#081B33;
      max-width:800px;
      width:100%;
      padding:40px;
      border-radius:30px;
      border:1px solid rgba(255,255,255,.1);
      max-height:90vh;
      overflow-y:auto;
    }

    .close{
      float:right;
      cursor:pointer;
      font-size:30px;
    }

    .contact{
      text-align:center;
    }

    .contact p{
      margin:15px 0;
      color:#ccc;
    }

    @media(max-width:900px){
      .hero-grid,
      .about-grid,
      .services-grid,
      .blog-grid{
        grid-template-columns:1fr;
      }

      .menu{
        display:none;
      }

      .hero h1{
        font-size:45px;
      }
    }

  </style>
</head>

<body>

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

<section class="hero" id="home">
  <div class="container hero-grid">

    <div>
      <h1>
        SOLUSI <span class="gold">PERPAJAKAN</span><br>
        PERUSAHAAN ANDA
      </h1>

      <p>
        ASA TAX SOLUTION adalah konsultan pajak profesional terpercaya
        dengan pengalaman lebih dari 20 tahun dalam bidang perpajakan
        dan akuntansi.
      </p>

      <a href="https://wa.me/6282136961885" class="btn">
        Konsultasi Sekarang
      </a>
    </div>

    <div class="card">
      <h2 class="gold" style="margin-bottom:25px;">
        ASA CHATBOT AI
      </h2>

      <div class="chat-box" id="chatBox">
        <div class="chat bot">
          Halo 👋 Saya ASA CHATBOT AI. Silakan tanyakan
          seputar pajak, NPWP, PPN, SP2DK, dan layanan ASA TAX Solution.
        </div>
      </div>

      <div class="chat-input">
        <input type="text" id="message" placeholder="Tanyakan sesuatu...">
        <button onclick="sendChat()">Kirim</button>
      </div>
    </div>

  </div>
</section>

<section id="about">
  <div class="container about-grid">

    <div class="about">
      <h2 class="title" style="text-align:left;">
        Tentang <span class="gold">Kami</span>
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
          MENJADI KONSULTAN PAJAK YANG PROFESIONAL,
          TERPERCAYA DAN HANDAL
        </p>
      </div>

      <div class="card vision-card">
        <h3>MISI</h3>
        <p>
          MEMBERI EDUKASI, MEMBERI SOLUSI DAN BERKOMITMEN
          DALAM PELAYANAN PERPAJAKAN
        </p>
      </div>

      <div class="card">
        <h3 class="gold">BUDAYA KERJA</h3>

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

<section id="services">
  <div class="container">

    <h2 class="title">
      Layanan <span class="gold">Kami</span>
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

<section id="blog">
  <div class="container">

    <h2 class="title">
      Artikel <span class="gold">Perpajakan</span>
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

<section id="contact">
  <div class="container card contact">

    <h2 class="title">
      Hubungi <span class="gold">Kami</span>
    </h2>

    <p>(0271) 7451358</p>
    <p>+62 821-3696-1885</p>
    <p>asataxs@gmail.com</p>
    <p>
      Jalan Perkutut No.17-A, Gonilan, Kartasura, Sukoharjo
    </p>

  </div>
</section>

<div class="modal" id="modal">
  <div class="modal-content">

    <span class="close" onclick="closeModal()">✕</span>

    <h2 id="modalTitle" class="gold"></h2>

    <p id="modalContent" style="margin-top:20px; line-height:2;"></p>

  </div>
</div>

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
