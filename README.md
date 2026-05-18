<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>ASA TAX SOLUTION</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
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
      overflow-x:hidden;
    }

    .container{
      width:90%;
      max-width:1300px;
      margin:auto;
    }

    nav{
      position:fixed;
      top:0;
      width:100%;
      z-index:999;
      background:rgba(8,27,51,.95);
      backdrop-filter:blur(12px);
      border-bottom:1px solid rgba(255,255,255,.08);
    }

    .navbar{
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:18px 0;
    }

    .logo{
      display:flex;
      align-items:center;
      gap:15px;
    }

    .logo img{
      height:65px;
    }

    .menu{
      display:flex;
      gap:30px;
    }

    .menu a{
      color:#ddd;
      text-decoration:none;
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
      padding-top:190px;
    }

    .hero-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:60px;
      align-items:center;
    }

    .hero h1{
      font-size:68px;
      line-height:1.1;
      margin-bottom:25px;
      font-weight:800;
    }

    .gold{
      color:#F5B942;
    }

    .hero p{
      color:#d1d1d1;
      line-height:2;
      font-size:17px;
      margin-bottom:35px;
    }

    .btn{
      background:#F5B942;
      color:black;
      text-decoration:none;
      padding:18px 35px;
      border-radius:16px;
      font-weight:700;
      display:inline-block;
      transition:.3s;
    }

    .btn:hover{
      transform:translateY(-3px);
    }

    .card{
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.08);
      border-radius:30px;
      padding:35px;
    }

    .chat-area{
      height:340px;
      overflow-y:auto;
      margin-bottom:20px;
    }

    .chat{
      padding:15px;
      border-radius:18px;
      margin-bottom:15px;
      line-height:1.8;
      font-size:14px;
    }

    .bot{
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.08);
    }

    .user{
      background:#F5B942;
      color:black;
      margin-left:60px;
    }

    .chat-input{
      display:flex;
      gap:12px;
    }

    .chat-input input{
      flex:1;
      padding:16px;
      border:none;
      border-radius:15px;
      background:rgba(255,255,255,.05);
      color:white;
      outline:none;
    }

    .chat-input button{
      background:#F5B942;
      border:none;
      border-radius:15px;
      padding:0 25px;
      font-weight:700;
      cursor:pointer;
    }

    .section-title{
      font-size:52px;
      text-align:center;
      margin-bottom:70px;
      font-weight:800;
    }

    .about-grid{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:50px;
    }

    .about p{
      color:#d2d2d2;
      line-height:2;
      margin-bottom:20px;
    }

    .info-card{
      margin-bottom:25px;
    }

    .info-card h3{
      color:#F5B942;
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
      background:rgba(245,185,66,.08);
      border:1px solid rgba(245,185,66,.15);
      padding:18px;
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

    .services-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:25px;
    }

    .service{
      background:rgba(255,255,255,.05);
      border:1px solid rgba(255,255,255,.08);
      border-radius:25px;
      padding:30px;
      transition:.3s;
    }

    .service:hover{
      transform:translateY(-5px);
      border-color:#F5B942;
    }

    .service-icon{
      font-size:40px;
      margin-bottom:20px;
    }

    .service h3{
      margin-bottom:15px;
      font-size:22px;
    }

    .service p{
      color:#cfcfcf;
      line-height:1.8;
      font-size:14px;
    }

    .blog-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:25px;
    }

    .blog{
      background:rgba(255,255,255,.05);
      border-radius:25px;
      overflow:hidden;
      border:1px solid rgba(255,255,255,.08);
    }

    .blog-image{
      height:220px;
      background:linear-gradient(135deg,#F5B94244,transparent);
    }

    .blog-content{
      padding:25px;
    }

    .blog h3{
      margin-bottom:15px;
      font-size:24px;
    }

    .blog p{
      color:#d1d1d1;
      line-height:1.8;
      margin-bottom:20px;
      font-size:14px;
    }

    .read-btn{
      background:#F5B942;
      border:none;
      padding:12px 20px;
      border-radius:12px;
      font-weight:700;
      cursor:pointer;
      margin-bottom:20px;
    }

    .source{
      border-top:1px solid rgba(255,255,255,.08);
      padding-top:15px;
      color:#9e9e9e;
      font-size:13px;
      line-height:1.7;
    }

    .modal{
      position:fixed;
      inset:0;
      background:rgba(0,0,0,.8);
      display:none;
      justify-content:center;
      align-items:center;
      padding:30px;
      z-index:9999;
    }

    .modal-content{
      background:#081B33;
      max-width:850px;
      width:100%;
      border-radius:30px;
      padding:40px;
      border:1px solid rgba(255,255,255,.08);
      max-height:90vh;
      overflow-y:auto;
    }

    .close{
      float:right;
      font-size:30px;
      cursor:pointer;
    }

    .contact{
      text-align:center;
    }

    .contact p{
      margin:15px 0;
      color:#d1d1d1;
    }

    footer{
      text-align:center;
      padding:30px;
      border-top:1px solid rgba(255,255,255,.08);
      color:#aaa;
      font-size:14px;
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
        font-size:48px;
      }

      .section-title{
        font-size:40px;
      }

    }

  </style>
</head>

<body>

<nav>
  <div class="container navbar">

    <div class="logo">
      <img src="logo.png" alt="ASA TAX">
    </div>

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
        dengan pengalaman lebih dari 20 tahun dalam bidang perpajakan,
        akuntansi dan legalitas bisnis perusahaan.
      </p>

      <a href="https://wa.me/6282136961885" class="btn">
        Konsultasi Sekarang
      </a>

    </div>

    <div class="card">

      <h2 class="gold" style="margin-bottom:25px;">
        ASA CHATBOT AI
      </h2>

      <div class="chat-area" id="chatArea">

        <div class="chat bot">
          Halo 👋 Saya ASA CHATBOT AI.
          Silakan tanyakan seputar pajak, NPWP, SP2DK,
          restitusi pajak, tax planning dan layanan ASA TAX Solution.
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

      <h2 class="section-title" style="text-align:left;">
        Tentang <span class="gold">Kami</span>
      </h2>

      <p>
        CV Asa Tax Solution adalah perusahaan Konsultan Pajak dan Akuntansi
        yang berlokasi di Kartasura, Sukoharjo, dan telah berdiri sejak 7 Januari 2005.
      </p>

      <p>
        Sejak awal perjalanannya, CV Asa Tax Solution konsisten memberikan
        layanan konsultasi kepada berbagai jenis perusahaan manufaktur,
        konstruksi, retail, perdagangan umum, jasa, developer,
        provider hingga sektor usaha lainnya.
      </p>

      <p>
        Dengan pengalaman dan keahlian yang dimiliki,
        CV Asa Tax Solution hadir sebagai mitra terpercaya
        untuk membantu perusahaan mengelola aspek keuangan
        dan perpajakan secara profesional.
      </p>

    </div>

    <div>

      <div class="card info-card">
        <h3>VISI</h3>
        <p>
          MENJADI KONSULTAN PAJAK YANG PROFESIONAL,
          TERPERCAYA DAN HANDAL
        </p>
      </div>

      <div class="card info-card">
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

    <h2 class="section-title">
      Layanan <span class="gold">Kami</span>
    </h2>

    <div class="services-grid">

      <div class="service">
        <div class="service-icon">💼</div>
        <h3>Konsultasi Perpajakan</h3>
        <p>
          Memberikan solusi perpajakan profesional
          sesuai regulasi perpajakan Indonesia.
        </p>
      </div>

      <div class="service">
        <div class="service-icon">📑</div>
        <h3>Review Pajak</h3>
        <p>
          Memastikan laporan dan dokumen perpajakan
          sesuai ketentuan yang berlaku.
        </p>
      </div>

      <div class="service">
        <div class="service-icon">📊</div>
        <h3>Tax Planning</h3>
        <p>
          Perencanaan pajak legal untuk efisiensi
          keuangan perusahaan.
        </p>
      </div>

      <div class="service">
        <div class="service-icon">🧾</div>
        <h3>Restitusi Pajak</h3>
        <p>
          Membantu proses pengembalian pajak
          secara profesional dan aman.
        </p>
      </div>

      <div class="service">
        <div class="service-icon">🏢</div>
        <h3>Pendirian Usaha</h3>
        <p>
          Membantu legalitas dan pendirian usaha
          perusahaan secara lengkap.
        </p>
      </div>

      <div class="service">
        <div class="service-icon">⚖️</div>
        <h3>Pendampingan SP2DK</h3>
        <p>
          Pendampingan pemeriksaan dan konsultasi
          perpajakan profesional.
        </p>
      </div>

    </div>

  </div>

</section>

<section id="blog">

  <div class="container">

    <h2 class="section-title">
      Artikel <span class="gold">Perpajakan</span>
    </h2>

    <div class="blog-grid">

      <div class="blog">

        <div class="blog-image"></div>

        <div class="blog-content">

          <h3>Strategi Efisiensi Pajak</h3>

          <p>
            Strategi legal untuk efisiensi pajak perusahaan.
          </p>

          <button class="read-btn"
            onclick="openBlog(
              'Strategi Efisiensi Pajak',
              'Efisiensi pajak perusahaan dapat dilakukan melalui tax planning yang legal dan sesuai regulasi perpajakan Indonesia.'
            )">
            Baca Selengkapnya
          </button>

          <div class="source">
            Sumber: Direktorat Jenderal Pajak Republik Indonesia
          </div>

        </div>

      </div>

      <div class="blog">

        <div class="blog-image"></div>

        <div class="blog-content">

          <h3>Cara Menghadapi SP2DK</h3>

          <p>
            Panduan menghadapi SP2DK dari DJP.
          </p>

          <button class="read-btn"
            onclick="openBlog(
              'Cara Menghadapi SP2DK',
              'SP2DK merupakan surat dari DJP yang memerlukan klarifikasi data perpajakan dan pendampingan profesional.'
            )">
            Baca Selengkapnya
          </button>

          <div class="source">
            Sumber: PMK dan Peraturan Perpajakan Indonesia
          </div>

        </div>

      </div>

      <div class="blog">

        <div class="blog-image"></div>

        <div class="blog-content">

          <h3>Pentingnya Tax Planning</h3>

          <p>
            Pentingnya tax planning untuk bisnis modern.
          </p>

          <button class="read-btn"
            onclick="openBlog(
              'Pentingnya Tax Planning',
              'Tax planning membantu perusahaan mengelola kewajiban pajak secara efisien dan legal.'
            )">
            Baca Selengkapnya
          </button>

          <div class="source">
            Sumber: UU Harmonisasi Peraturan Perpajakan
          </div>

        </div>

      </div>

    </div>

  </div>

</section>

<section id="contact">

  <div class="container card contact">

    <h2 class="section-title">
      Hubungi <span class="gold">Kami</span>
    </h2>

    <p>(0271) 7451358</p>
    <p>+62 821-3696-1885</p>
    <p>asataxs@gmail.com</p>

    <p>
      Jalan Perkutut No.17-A, Gonilan,
      Kartasura, Sukoharjo
    </p>

  </div>

</section>

<footer>
  © 2026 ASA TAX SOLUTION — Professional Tax Consultant
</footer>

<div class="modal" id="modal">

  <div class="modal-content">

    <span class="close" onclick="closeModal()">✕</span>

    <h2 id="modalTitle" class="gold"></h2>

    <p id="modalText" style="margin-top:25px; line-height:2;"></p>

  </div>

</div>

<script>

function sendChat(){

  let input = document.getElementById("message");
  let text = input.value;

  if(text.trim() === "") return;

  let lower = text.toLowerCase();

  let chatArea = document.getElementById("chatArea");

  chatArea.innerHTML += `
    <div class="chat user">
      ${text}
    </div>
  `;

  let reply =
    "Tim ASA TAX Solution siap membantu kebutuhan perpajakan anda.";

  if(lower.includes("npwp")){
    reply =
      "Pengurusan NPWP perusahaan memerlukan dokumen legalitas usaha dan identitas direktur.";
  }

  else if(lower.includes("ppn")){
    reply =
      "PPN adalah Pajak Pertambahan Nilai yang dikenakan pada transaksi barang dan jasa.";
  }

  else if(lower.includes("sp2dk")){
    reply =
      "SP2DK adalah surat klarifikasi data perpajakan dari DJP.";
  }

  else if(lower.includes("restitusi")){
    reply =
      "Restitusi pajak adalah pengembalian kelebihan pembayaran pajak.";
  }

  else if(lower.includes("tax")){
    reply =
      "Tax planning membantu perusahaan mengelola kewajiban pajak secara efisien.";
  }

  setTimeout(() => {

    chatArea.innerHTML += `
      <div class="chat bot">
        ${reply}
        <br><br>
        Untuk konsultasi lebih lanjut silakan hubungi WhatsApp:
        <br>
        <b>+62 821-3696-1885</b>
      </div>
    `;

    chatArea.scrollTop = chatArea.scrollHeight;

  },500);

  input.value = "";

}

function openBlog(title,text){

  document.getElementById("modal").style.display = "flex";
  document.getElementById("modalTitle").innerText = title;
  document.getElementById("modalText").innerText = text;

}

function closeModal(){

  document.getElementById("modal").style.display = "none";

}

</script>

</body>
</html>
