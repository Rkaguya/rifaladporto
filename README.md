[porto.html](https://github.com/user-attachments/files/22184561/porto.html)
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Rifal Aditia</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: url('https://wallpaperaccess.com/full/1567665.png') no-repeat center center fixed;
      background-size: cover;
      color: #f5f5f5;
      position: relative;
    }

    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.85); 
      z-index: -1;
    }

    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 30px;
      background: rgba(0, 0, 0, 0.85);
      border-bottom: 2px solid #FFD700;
      z-index: 1000;
    }
    nav h1 {
      font-size: 1.5rem;
      color: #FFD700;
      margin: 0;
    }

    .marquee {
      width: 100%;
      overflow: hidden;
      white-space: nowrap;
      background: rgba(20, 20, 20, 0.9);
      color: #FFD700;
      padding: 10px 0;
      font-size: 1.2rem;
      font-weight: bold;
      margin-top: 60px;
    }
    .marquee span {
      display: inline-block;
      padding-left: 100%;
      animation: marquee 15s linear infinite;
    }
    @keyframes marquee {
      0% { transform: translateX(0%); }
      100% { transform: translateX(-100%); }
    }

    main {
      max-width: 1000px;
      margin: auto;
      padding: 100px 20px 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 30px;
    }

    /* Profil */
    .profile {
      text-align: center;
      background: rgba(20, 20, 20, 0.95);
      border: 1px solid #FFD700;
      border-radius: 16px;
      padding: 30px 20px;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.3);
      max-width: 800px;
      width: 90%;
    }
    .profile img {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 3px solid #FFD700;
      object-fit: cover;
      margin-bottom: 15px;
      transition: transform 0.3s ease;
    }
    .profile img:hover {
      transform: scale(1.1) rotate(3deg);
    }
    /* Efek ketikan */
    .typing {
      font-size: 1.8rem;
      font-weight: bold;
      color: #FFD700;
      border-right: 3px solid #FFD700;
      white-space: nowrap;
      overflow: hidden;
      width: 0;
      animation: typing 3s steps(20, end) forwards, blink 0.7s step-end infinite;
      margin: 10px auto;
    }
    @keyframes typing {
      from { width: 0; }
      to { width: 15ch; }
    }
    @keyframes blink {
      50% { border-color: transparent; }
    }
    .profile p {
      max-width: 600px;
      margin: auto;
      color: #d1d5db;
    }

    section {
      background: rgba(20, 20, 20, 0.95);
      border: 1px solid #FFD700;
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 0 15px rgba(255, 215, 0, 0.3);
      transition: transform 0.3s ease;
      width: 90%;
      max-width: 800px;
      text-align: center;
    }
    section:hover {
      transform: translateY(-5px);
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.6);
    }
    h2 {
      margin-bottom: 15px;
      font-size: 1.6rem;
      color: #FFD700;
      text-transform: uppercase;
      border-bottom: 2px solid #FFD700;
      display: inline-block;
      padding-bottom: 5px;
    }
    h3 {
      color: #FFD700;
    }
    ul {
      padding-left: 20px;
      text-align: left;
      color: #d1d5db;
    }

    .skills {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
      gap: 10px;
    }
    .skill {
      background: #FFD700;
      color: #000;
      padding: 15px;
      border-radius: 12px;
      text-align: center;
      font-weight: bold;
      transition: transform 0.3s, box-shadow 0.3s;
      position: relative;
      overflow: hidden;
    }
    .skill::after {
      content: "";
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: rgba(255, 255, 255, 0.3);
      transform: rotate(25deg);
      transition: transform 0.5s;
    }
    .skill:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.6);
    }
    .skill:hover::after {
      transform: translateX(100%) rotate(25deg);
    }

    .experience-container {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
    }
    .experience-card {
      background: #111;
      border: 1px solid #FFD700;
      border-radius: 12px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(255,215,0,0.3);
      transition: transform 0.3s;
      animation: fadeInUp 1s ease forwards;
    }
    .experience-card:hover {
      transform: translateY(-5px);
    }
    .experience-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-bottom: 2px solid #FFD700;
    }
    .experience-content {
      padding: 15px;
      text-align: left;
    }
    .experience-content h3 {
      margin: 0;
      color: #FFD700;
    }
    .experience-content p {
      margin: 5px 0;
      color: #d1d5db;
    }

    footer {
      text-align: center;
      padding: 20px;
      border-top: 1px solid #FFD700;
      font-size: 0.9rem;
      color: #FFD700;
      background: #000;
    }
    .btn {
      display: inline-block;
      margin-top: 10px;
      background: #FFD700;
      color: black;
      padding: 10px 18px;
      border-radius: 25px;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s, transform 0.3s;
    }
    .btn:hover {
      background: #e6c200;
      transform: scale(1.05);
    }

    @keyframes fadeInUp {
      from {opacity: 0; transform: translateY(30px);}
      to {opacity: 1; transform: translateY(0);}
    }

    @media (min-width: 768px) {
      .experience-container {
        grid-template-columns: 1fr 1fr;
      }
    }
  </style>
</head>
<body>
  <nav>
    <h1>Rifal Aditia S.Pd.</h1>
  </nav>

  <div class="marquee">
    <span>Halo! Selamat datang • Seorang pendidik dan penulis yang berkomitmen pada kreativitas • Menginspirasi lewat bahasa dan sastra</span>
  </div>

  <main>
    <!-- Profil -->
    <section class="profile">
      <img src="https://image2url.com/images/1757130696277-f0b96fb4-f1c1-4540-a00a-4fcdcecaaee7.jpeg" alt="Foto Profil">
      <h2 class="typing">RIFAL ADITIA</h2>
      <p>Saya lulusan Program Studi Pendidikan Bahasa dan Sastra Indonesia di Universitas Indraprasta PGRI (UNINDRA). Saya memiliki minat besar dalam dunia pendidikan, khususnya dalam mengembangkan potensi dan literasi siswa. Saya berkomitmen untuk terus belajar, memperluas wawasan, serta mencari pengalaman baru. Dengan pengetahuan dan keterampilan yang saya peroleh, saya bertekad untuk memberikan kontribusi nyata yang bermanfaat bagi masyarakat dan dunia pendidikan.</p>
    </section>

    <!-- Pendidikan -->
    <section id="pendidikan">
      <h2>Pendidikan</h2>
      <ul>
        <li>S1 Pendidikan Bahasa dan Sastra Indonesia - Universitas Indraprasta PGRI (2021 - 2025)</li>
        <li>SMA AL-Huda Cengkareng (2018 - 2021)</li>
        <li>SMP AL-Huda Cengkareng (2015 - 2018)</li>
      </ul>
    </section>

    <!-- Pengalaman -->
    <section id="pengalaman">
      <h2>Pengalaman</h2>
      <div class="experience-container">
        <div class="experience-card">
          <img src="https://image2url.com/images/1757130729666-4431a577-1120-44eb-805d-2f98f4cac2e1.jpeg" alt="271">
          <div class="experience-content">
            <h3>Merdeka Belajar Kampus Merdeka Kemendikbudristek</h3>
            <p><em>SMP Negeri 271 Jakarta (2024)</em></p>
            <p>Merancang kegiatan untuk peningkatan literasi dan numerasi di SMPN 271 Jakarta</p>
          </div>
        </div>

        <div class="experience-card">
          <img src="https://image2url.com/images/1757130749051-ef466fa9-5cce-4198-9574-59ff5334a3a8.jpeg" alt="169">
          <div class="experience-content">
            <h3>Pelatih Ekstrakurikuler Indo Club</h3>
            <p><em>SMP Negeri 169 Jakarta & SMP Negeri 186 Jakarta (2023 - Sekarang)</em></p>
            <p>Membimbing siswa dalam merancang karya sastra</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Keahlian -->
    <section id="keahlian">
      <h2>Keahlian</h2>
      <div class="skills">
        <div class="skill">Menulis</div>
        <div class="skill">Komunikasi</div>
        <div class="skill">Editing Teks</div>
        <div class="skill">Manajemen Waktu</div>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 RIFAL ADITIA</p>
    <a href="https://wa.me/6281312327972" class="btn">Hubungi Saya</a>
  </footer>

  <script>
    
    const sections = document.querySelectorAll('section');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = 1;
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, { threshold: 0.2 });

    sections.forEach(section => {
      section.style.opacity = 0;
      section.style.transform = 'translateY(30px)';
      section.style.transition = 'all 0.8s ease';
      observer.observe(section);
    });
  </script>
</body>
</html>
