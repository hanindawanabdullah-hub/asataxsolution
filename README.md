<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Jago Pajak | Konsultan Pajak Profesional</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins',sans-serif;
    }

    body{
      background:#fff;
      color:#333;
      overflow-x:hidden;
    }

    :root{
      --orange:#ff7a00;
      --yellow:#ffcc00;
      --dark:#1d1d1d;
      --light:#fff8ef;
    }

    header{
      width:100%;
      padding:18px 8%;
      display:flex;
      justify-content:space-between;
      align-items:center;
      position:fixed;
      top:0;
      z-index:999;
      background:rgba(255,255,255,0.95);
      backdrop-filter:blur(10px);
      box-shadow:0 2px 10px rgba(0,0,0,0.05);
    }

    .logo{
      font-size:28px;
      font-weight:700;
      color:var(--orange);
    }

    .logo span{
      color:var(--yellow);
    }

    nav a{
      margin-left:25px;
      text-decoration:none;
      color:#444;
      font-weight:500;
      transition:.3s;
    }

    nav a:hover{
      color:var(--orange);
    }

    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:120px 8% 60px;
      background:linear-gradient(135deg,#fff,#fff7eb);
      gap:40px;
      flex-wrap:wrap;
    }

    .hero-text{
      flex:1;
      min-width:320px;
    }

    .hero-text h1{
      font-size:60px;
      line-height:1.1;
      margin-bottom:20px;
      color:var(--dark);
    }

    .hero-text h1 span{
      color:var(--orange);
    }

    .hero-text p{
      font-size:18px;
      line-height:1.8;
      margin-bottom:30px;
      color:#555;
    }

    .btn-group{
      display:flex;
      gap:15px;
      flex-wrap:wrap;
    }

    .btn{
      padding:15px 28px;
      border:none;
      border-radius:14px;
      cursor:pointer;
      font-size:16px;
      font-weight:600;
      text-decoration:none;
      transition:.3s;
      display:inline-block;
    }

    .btn-primary{
      background:linear-gradient(135deg,var(--orange),var(--yellow));
      color:white;
      box-shadow:0 10px 20px rgba(255,122,0,.25);
    }

    .btn-primary:hover{
      transform:translateY(-3px);
    }

    .btn-secondary{
      background:white;
      border:2px solid var(--orange);
      color:var(--orange);
    }

    .hero-image{
      flex:1;
      min-width:320px;
      display:flex;
      justify-content:center;
    }

    .hero-card{
      width:420px;
      background:white;
      border-radius:30px;
      padding:35px;
      box-shadow:0 20px 60px rgba(0,0,0,0.08);
      border:1px solid #f2f2f2;
    }

    .hero-card h3{
      margin-bottom:25px;
      font-size:26px;
      color:var(--orange);
    }

    .hero-card ul{
      list-style:none;
    }

    .hero-card ul li{
      margin-bottom:18px;
      font-size:17px;
    }

    section{
      padding:90px 8%;
    }

    .section-title{
      text-align:center;
      margin-bottom:50px;
    }

    .section-title h2{
      font-size:42px;
      color:var(--dark);
      margin-bottom:15px;
    }

    .section-title p{
      color:#666;
    }

    .services{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:30px;
    }

    .service-card{
      background:white;
      border-radius:24px;
      padding:35px;
      transition:.3s;
      border:1px solid #f1f1f1;
      box-shadow:0 10px 25px rgba(0,0,0,0.04);
    }

    .service-card:hover{
      transform:translateY(-8px);
      box-shadow:0 15px 35px rgba(255,122,0,.15);
    }

    .service-card h3{
      color:var(--orange);
      margin-bottom:15px;
      font-size:24px;
    }

    .service-card p{
      color:#666;
      margin-bottom:20px;
      line-height:1.7;
    }

    .price{
      font-size:28px;
      font-weight:700;
      color:var(--dark);
      margin-bottom:20px;
    }

    .market{
      background:linear-gradient(135deg,var(--orange),#ffb300);
      border-radius:35px;
      color:white;
      text-align:center;
      padding:70px 8%;
      margin:0 8%;
    }

    .market h2{
      font-size:42px;
      margin-bottom:20px;
    }

    .market p{
      font-size:18px;
      max-width:850px;
      margin:auto;
      line-height:1.9;
    }

    .testimonials{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:30px;
    }

    .testimonial{
      background:#fff8ef;
      padding:30px;
      border-radius:24px;
    }

    .testimonial h4{
      color:var(--orange);
      margin-bottom:10px;
    }

    .chatbot{
      background:white;
      border-radius:30px;
      padding:40px;
      box-shadow:0 10px 40px rgba(0,0,0,0.06);
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:40px;
      align-items:center;
    }

    .chatbot img{
      width:100%;
    }

    .chatbox{
      background:#fff8ef;
      border-radius:20px;
      padding:25px;
    }

    .bot-message{
      background:white;
      padding:14px 18px;
      border-radius:15px;
      margin-bottom:15px;
      box-shadow:0 4px 10px rgba(0,0,0,0.05);
    }

    .faq{
      display:grid;
      gap:20px;
    }

    .faq-item{
      background:white;
      padding:25px;
      border-radius:18px;
      box-shadow:0 5px 20px rgba(0,0,0,0.05);
    }

    footer{
      background:#111;
      color:white;
      padding:50px 8%;
      text-align:center;
      margin-top:80px;
    }

    footer h3{
      color:var(--yellow);
      margin-bottom:15px;
      font-size:28px;
    }

    .floating-wa{
      position:fixed;
      bottom:25px;
      right:25px;
      background:#25d366;
      width:70px;
      height:70px;
      border-radius:50%;
      display:flex;
      justify-content:center;
      align-items:center;
      text-decoration:none;
      color:white;
      font-size:32px;
      box-shadow:0 10px 30px rgba(0,0,0,.2);
      z-index:999;
    }

    @media(max-width:900px){
      .hero{
        flex-direction:column;
      }

      .hero-text h1{
        font-size:42px;
      }

      .chatbot{
        grid-template-columns:1fr;
      }

      nav{
        display:none;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="logo">Jago<span>Pajak</span></div>

  <nav>
    <a href="#">Home</a>
    <a href="#layanan">Layanan</a>
    <a href="#market">Market</a>
    <a href="#ai">AI Chatbot</a>
    <a href="#kontak">Kontak</a>
  </nav>
</header>

<section class="hero">

  <div class="hero-text">
    <h1>Konsultan <span>Pajak Modern</span> & Terpercaya</h1>

    <p>
      🔶 Jago Pajak <br><br>
      💼 Berpengalaman terpercaya <br>
      📄 Jasa NPWP • SPT • PKP • Konsultasi <br>
      💬 Fast response & amanah
    </p>

    <div class="btn-group">
      <a href="https://wa.me/6287831673591" class="btn btn-primary">
        Konsultasi WA 1
      </a>

      <a href="https://wa.me/6288902943191" class="btn btn-secondary">
        Konsultasi WA 2
      </a>
    </div>
  </div>

  <div class="hero-image">
    <div class="hero-card">
      <h3>Layanan Profesional</h3>

      <ul>
        <li>✅ Pembuatan NPWP</li>
        <li>✅ Pelaporan SPT Tahunan</li>
        <li>✅ Pengurusan PKP</li>
        <li>✅ Konsultasi Pajak UMKM</li>
        <li>✅ Pajak Badan Usaha</li>
        <li>✅ Pendampingan Pemeriksaan</li>
      </ul>
    </div>
  </div>

</section>

<section id="layanan">

  <div class="section-title">
    <h2>Layanan Kami</h2>
    <p>Pelayanan pajak profesional dengan harga terjangkau</p>
  </div>

  <div class="services">

    <div class="service-card">
      <h3>NPWP</h3>
      <p>Pembuatan dan aktivasi NPWP pribadi maupun perusahaan dengan proses cepat.</p>
      <div class="price">Rp99K</div>
      <a href="https://wa.me/6287831673591" class="btn btn-primary">Pesan Sekarang</a>
    </div>

    <div class="service-card">
      <h3>SPT Tahunan</h3>
      <p>Bantu lapor SPT tahunan pribadi maupun badan usaha tanpa ribet.</p>
      <div class="price">Rp149K</div>
      <a href="https://wa.me/6288902943191" class="btn btn-primary">Pesan Sekarang</a>
    </div>

    <div class="service-card">
      <h3>Pengurusan PKP</h3>
      <p>Legalitas PKP lengkap untuk bisnis dan perusahaan Anda.</p>
      <div class="price">Rp499K</div>
      <a href="https://wa.me/6287831673591" class="btn btn-primary">Pesan Sekarang</a>
    </div>

    <div class="service-card">
      <h3>Konsultasi Pajak</h3>
      <p>Konsultasi bisnis, UMKM, dan strategi perpajakan bersama ahli.</p>
      <div class="price">Rp79K</div>
      <a href="https://wa.me/6288902943191" class="btn btn-primary">Konsultasi</a>
    </div>

  </div>

</section>

<section class="market" id="market">

  <h2>Market & Target Client</h2>

  <p>
    Kami melayani berbagai kebutuhan perpajakan mulai dari UMKM, freelancer,
    content creator, perusahaan startup, toko online, hingga badan usaha profesional.
    Dengan sistem digital modern, proses konsultasi dan pengurusan pajak dapat dilakukan
    secara online dengan cepat, aman, dan terpercaya.
  </p>

</section>

<section>

  <div class="section-title">
    <h2>Testimoni Client</h2>
    <p>Dipercaya oleh banyak client dari seluruh Indonesia</p>
  </div>

  <div class="testimonials">

    <div class="testimonial">
      <h4>Rizky - UMKM</h4>
      <p>
        “Pelayanannya cepat banget dan sangat membantu urusan SPT tahunan saya.”
      </p>
    </div>

    <div class="testimonial">
      <h4>Andini - Freelancer</h4>
      <p>
        “Admin fast response dan proses NPWP selesai dalam waktu singkat.”
      </p>
    </div>

    <div class="testimonial">
      <h4>Budi - Owner Startup</h4>
      <p>
        “Konsultasinya jelas dan profesional. Recommended untuk bisnis.”
      </p>
    </div>

  </div>

</section>

<section id="ai">

  <div class="section-title">
    <h2>AI Chatbot Pajak</h2>
    <p>Chatbot AI untuk membantu pertanyaan perpajakan secara otomatis</p>
  </div>

  <div class="chatbot">

    <div>
      <h2 style="font-size:38px;margin-bottom:20px;color:#ff7a00;">
        Smart Tax Assistant
      </h2>

      <p style="line-height:1.9;color:#666;">
        AI chatbot dapat menjawab pertanyaan tentang:
      </p>

      <br>

      <ul style="line-height:2;color:#444;">
        <li>✅ Cara lapor SPT</li>
        <li>✅ Cara membuat NPWP</li>
        <li>✅ Konsultasi pajak UMKM</li>
        <li>✅ Peraturan pajak terbaru</li>
        <li>✅ Simulasi pajak bisnis</li>
        <li>✅ FAQ perpajakan</li>
      </ul>

      <br>

      <a href="https://wa.me/6287831673591" class="btn btn-primary">
        Integrasi AI Sekarang
      </a>
    </div>

    <div class="chatbox">

      <div class="bot-message">
        🤖 Halo, ada yang bisa saya bantu terkait pajak?
      </div>

      <div class="bot-message">
        💬 Cara lapor SPT tahunan bagaimana?
      </div>

      <div class="bot-message">
        🤖 Anda dapat menyiapkan EFIN dan bukti penghasilan terlebih dahulu.
      </div>

      <div class="bot-message">
        💬 Berapa biaya pengurusan PKP?
      </div>

      <div class="bot-message">
        🤖 Mulai dari Rp499.000 tergantung kebutuhan bisnis Anda.
      </div>

    </div>

  </div>

</section>

<section>

  <div class="section-title">
    <h2>FAQ</h2>
    <p>Pertanyaan yang sering ditanyakan</p>
  </div>

  <div class="faq">

    <div class="faq-item">
      <h3>Apakah konsultasi bisa online?</h3>
      <p>Ya, seluruh layanan bisa dilakukan secara online via WhatsApp.</p>
    </div>

    <div class="faq-item">
      <h3>Berapa lama proses NPWP?</h3>
      <p>Rata-rata proses 1-2 hari kerja tergantung data client.</p>
    </div>

    <div class="faq-item">
      <h3>Apakah data aman?</h3>
      <p>Kami menjaga seluruh data client dengan sistem yang aman dan profesional.</p>
    </div>

  </div>

</section>

<footer id="kontak">

  <h3>Jago Pajak</h3>

  <p>
    Konsultan Pajak Profesional & Amanah
  </p>

  <br>

  <p>📞 WA 1 : 087831673591</p>
  <p>📞 WA 2 : 088902943191</p>

  <br>

  <p>© 2026 Jago Pajak. All Rights Reserved.</p>

</footer>

<a class="floating-wa" href="https://wa.me/6287831673591">
  ☎
</a>

<script>
  console.log("Website Jago Pajak Ready");
</script>

</body>
<style>

.ai-chat-toggle{
  position:fixed;
  bottom:110px;
  right:25px;
  width:75px;
  height:75px;
  border-radius:50%;
  border:none;
  cursor:pointer;
  z-index:99999;
  background:linear-gradient(135deg,#ff7a00,#ffcc00);
  color:white;
  font-size:34px;
  box-shadow:0 15px 35px rgba(0,0,0,.25);
  transition:.3s;
}

.ai-chat-toggle:hover{
  transform:scale(1.08);
}

.ai-chat-container{
  position:fixed;
  bottom:110px;
  right:25px;
  width:400px;
  height:650px;
  background:white;
  border-radius:30px;
  overflow:hidden;
  box-shadow:0 25px 60px rgba(0,0,0,.25);
  z-index:999999;
  display:none;
  flex-direction:column;
  animation:fadeIn .3s ease;
  border:1px solid #eee;
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

.ai-header{
  background:linear-gradient(135deg,#ff7a00,#ffcc00);
  padding:22px;
  color:white;
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.ai-header h3{
  font-size:24px;
}

.ai-status{
  font-size:13px;
  opacity:.9;
}

.close-ai{
  background:none;
  border:none;
  color:white;
  font-size:28px;
  cursor:pointer;
}

.ai-body{
  flex:1;
  overflow-y:auto;
  padding:20px;
  background:#fff8ef;
}

.ai-message{
  max-width:85%;
  padding:15px 18px;
  border-radius:20px;
  margin-bottom:16px;
  line-height:1.7;
  font-size:15px;
  animation:msg .2s ease;
}

@keyframes msg{
  from{
    opacity:0;
    transform:translateY(10px);
  }
  to{
    opacity:1;
    transform:translateY(0);
  }
}

.bot{
  background:white;
  color:#333;
  box-shadow:0 5px 15px rgba(0,0,0,.05);
}

.user{
  background:linear-gradient(135deg,#ff7a00,#ffb300);
  color:white;
  margin-left:auto;
}

.ai-input{
  padding:18px;
  background:white;
  display:flex;
  gap:10px;
  border-top:1px solid #eee;
}

.ai-input input{
  flex:1;
  padding:15px;
  border-radius:16px;
  border:1px solid #ddd;
  outline:none;
  font-size:15px;
}

.ai-input button{
  padding:15px 20px;
  border:none;
  border-radius:16px;
  background:linear-gradient(135deg,#ff7a00,#ffcc00);
  color:white;
  font-weight:600;
  cursor:pointer;
}

.ai-suggestion{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  margin-top:15px;
}

.ai-chip{
  background:white;
  padding:10px 15px;
  border-radius:50px;
  cursor:pointer;
  font-size:13px;
  box-shadow:0 3px 10px rgba(0,0,0,.05);
  transition:.3s;
}

.ai-chip:hover{
  background:#ff7a00;
  color:white;
}

.typing{
  display:flex;
  gap:5px;
  align-items:center;
}

.typing span{
  width:8px;
  height:8px;
  background:#999;
  border-radius:50%;
  animation:blink 1s infinite;
}

.typing span:nth-child(2){
  animation-delay:.2s;
}

.typing span:nth-child(3){
  animation-delay:.4s;
}

@keyframes blink{
  0%{opacity:.2}
  50%{opacity:1}
  100%{opacity:.2}
}

@media(max-width:500px){

  .ai-chat-container{
    width:95%;
    right:2.5%;
    height:85vh;
    bottom:100px;
  }

}

</style>

<!-- CHAT BUTTON -->
<button class="ai-chat-toggle" onclick="toggleAI()">
  🤖
</button>

<!-- CHATBOT -->
<div class="ai-chat-container" id="aiChat">

  <div class="ai-header">

    <div>
      <h3>AI Pajak Assistant</h3>
      <div class="ai-status">
        Online • Fast Response
      </div>
    </div>

    <button class="close-ai" onclick="toggleAI()">
      ✕
    </button>

  </div>

  <div class="ai-body" id="chatBody">

    <div class="ai-message bot">
      👋 Halo! Saya AI Pajak Assistant.<br><br>
      Saya bisa membantu pertanyaan tentang:
      <br><br>
      ✅ NPWP <br>
      ✅ SPT Tahunan <br>
      ✅ PKP <br>
      ✅ Pajak UMKM <br>
      ✅ Pajak Freelancer <br>
      ✅ Konsultasi Pajak
    </div>

    <div class="ai-suggestion">

      <div class="ai-chip" onclick="quickAsk('Cara membuat NPWP')">
        Cara membuat NPWP
      </div>

      <div class="ai-chip" onclick="quickAsk('Cara lapor SPT')">
        Cara lapor SPT
      </div>

      <div class="ai-chip" onclick="quickAsk('Biaya pengurusan PKP')">
        Biaya PKP
      </div>

      <div class="ai-chip" onclick="quickAsk('Pajak UMKM berapa persen')">
        Pajak UMKM
      </div>

    </div>

  </div>

  <div class="ai-input">

    <input 
      type="text" 
      id="userInput"
      placeholder="Tulis pertanyaan..."
      onkeypress="if(event.key==='Enter')sendMessage()"
    >

    <button onclick="sendMessage()">
      Kirim
    </button>

  </div>

</div>

<script>

const aiDatabase = {

  "npwp":
  "📄 Untuk membuat NPWP, Anda perlu menyiapkan:\n\n✅ KTP\n✅ Email aktif\n✅ Nomor HP\n\nProses biasanya 1-2 hari kerja.",

  "spt":
  "🧾 Pelaporan SPT Tahunan dapat dilakukan online melalui DJP Online.\n\nDokumen yang dibutuhkan:\n\n✅ EFIN\n✅ Bukti penghasilan\n✅ NPWP",

  "pkp":
  "🏢 Pengurusan PKP cocok untuk bisnis/perusahaan yang membutuhkan legalitas PPN.\n\n💰 Biaya mulai Rp499.000",

  "umkm":
  "📊 Pajak UMKM umumnya dikenakan tarif final sesuai regulasi terbaru.\n\nKami dapat membantu simulasi dan konsultasinya.",

  "freelancer":
  "💻 Freelancer tetap wajib melaporkan penghasilan tahunan jika memenuhi ketentuan perpajakan.",

  "harga":
  "💰 Daftar layanan:\n\n✅ NPWP : Rp99K\n✅ SPT : Rp149K\n✅ PKP : Rp499K\n✅ Konsultasi : Rp79K",

  "konsultasi":
  "📞 Anda dapat konsultasi langsung melalui WhatsApp:\n\nWA 1 : 087831673591\nWA 2 : 088902943191",

  "default":
  "🤖 Maaf, pertanyaan belum ditemukan di database AI.\n\nSilakan konsultasi langsung via WhatsApp untuk bantuan lebih lanjut."
};

function toggleAI(){

  const chat = document.getElementById("aiChat");

  if(chat.style.display === "flex"){
    chat.style.display = "none";
  }else{
    chat.style.display = "flex";
  }

}

function addMessage(message,type){

  const chatBody = document.getElementById("chatBody");

  const div = document.createElement("div");

  div.className = "ai-message " + type;

  div.innerHTML = message.replace(/\n/g,"<br>");

  chatBody.appendChild(div);

  chatBody.scrollTop = chatBody.scrollHeight;

}

function showTyping(){

  const chatBody = document.getElementById("chatBody");

  const typing = document.createElement("div");

  typing.className = "ai-message bot";

  typing.id = "typing";

  typing.innerHTML = `
    <div class="typing">
      <span></span>
      <span></span>
      <span></span>
    </div>
  `;

  chatBody.appendChild(typing);

  chatBody.scrollTop = chatBody.scrollHeight;

}

function removeTyping(){

  const typing = document.getElementById("typing");

  if(typing){
    typing.remove();
  }

}

function getAIResponse(text){

  text = text.toLowerCase();

  if(text.includes("npwp")){
    return aiDatabase.npwp;
  }

  if(text.includes("spt")){
    return aiDatabase.spt;
  }

  if(text.includes("pkp")){
    return aiDatabase.pkp;
  }

  if(text.includes("umkm")){
    return aiDatabase.umkm;
  }

  if(text.includes("freelancer")){
    return aiDatabase.freelancer;
  }

  if(text.includes("harga") || text.includes("biaya")){
    return aiDatabase.harga;
  }

  if(text.includes("konsultasi") || text.includes("wa")){
    return aiDatabase.konsultasi;
  }

  return aiDatabase.default;

}

function sendMessage(){

  const input = document.getElementById("userInput");

  const text = input.value.trim();

  if(text === "") return;

  addMessage(text,"user");

  input.value = "";

  showTyping();

  setTimeout(()=>{

    removeTyping();

    const response = getAIResponse(text);

    addMessage(response,"bot");

  },1000);

}

function quickAsk(text){

  document.getElementById("userInput").value = text;

  sendMessage();

}

console.log("AI Pajak Assistant Ready");

</script>
</html>
