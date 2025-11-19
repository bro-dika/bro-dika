<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Bro Dika — Profile</title>

<style>
  /* --- THEME VARIABLES --- */
  :root {
    --bg: #0d1117;
    --text: #ffffff;
    --card: rgba(255,255,255,0.06);
    --shadow: rgba(0,0,0,0.22);
  }

  /* LIGHT MODE */
  @media (prefers-color-scheme: light) {
    :root {
      --bg: #f4f4f4;
      --text: #111;
      --card: rgba(0,0,0,0.07);
      --shadow: rgba(0,0,0,0.15);
    }
  }

  body {
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
    background: var(--bg);
    color: var(--text);
    overflow-x: hidden;
  }

  /* --- PARTIKEL BACKGROUND --- */
  #particles {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    z-index: -1;
    overflow: hidden;
  }

  .particle {
    position: absolute;
    width: 4px;
    height: 4px;
    border-radius: 50%;
    background: white;
    opacity: 0.25;
    animation: floatUp linear infinite;
  }

  @keyframes floatUp {
    from { transform: translateY(100vh); opacity: 0.25; }
    to   { transform: translateY(-10vh); opacity: 0; }
  }

  /* --- LAYOUT --- */
  .container {
    max-width: 900px;
    margin: auto;
    padding: 25px;
    text-align: center;
  }

  h1 {
    font-size: 2rem;
    margin-bottom: 5px;
  }

  .card {
    background: var(--card);
    padding: 25px;
    border-radius: 16px;
    box-shadow: 0 0 25px var(--shadow);
    backdrop-filter: blur(6px);
    margin-top: 40px;
  }

  /* --- SKILLS ICON SECTION --- */
  .skills {
    display: flex;
    justify-content: center;
    gap: 25px;
    flex-wrap: wrap;
    margin-top: 20px;
  }

  .skill-item {
    text-align: center;
    width: 110px;
  }

  .skill-item img {
    width: 55px;
    height: 55px;
    transition: transform .3s;
  }

  .skill-item img:hover {
    transform: scale(1.15);
  }

  /* SOSMED */
  .socials {
    margin-top: 20px;
    display: flex;
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }

  .socials a {
    padding: 10px 18px;
    border-radius: 30px;
    text-decoration: none;
    font-weight: 600;
    background: var(--card);
    color: var(--text);
    border: 1px solid rgba(255,255,255,0.1);
    transition: 0.3s;
  }

  .socials a:hover {
    background: rgba(255,255,255,0.15);
  }

  /* RESPONSIVE */
  @media(max-width: 600px) {
    h1 { font-size: 1.6rem; }
    .skill-item { width: 90px; }
    .skill-item img { width: 45px; height: 45px; }
  }
</style>
</head>

<body>

<!-- PARTIKEL BACKGROUND -->
<div id="particles"></div>

<div class="container">

  <!-- TITLE -->
  <h1>Hello, here bro dika 👋 </h1>
  <p>Front-End Developer • Creative Technologist • AI Prompt Engineer</p>
  
    <!-- GITHUB STATS -->
  <div class="card">
    <h2>📊 GitHub Statistics</h2>

    <img 
      class="stats-img"
      src="https://github-readme-stats.vercel.app/api?username=yourgithub&show_icons=true&theme=tokyonight"
      style="width:100%;max-width:450px;border-radius:10px;margin-bottom:15px;"
    >

    <img 
      class="stats-img"
      src="https://github-readme-streak-stats.herokuapp.com?user=yourgithub&theme=tokyonight"
      style="width:100%;max-width:450px;border-radius:10px;"
    >
  </div>

  <!-- Skills -->
  <div class="card">
    <h2>🛠 Skills</h2>

    <div class="skills">
      <div class="skill-item">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg">
        <p>HTML</p>
      </div>

      <div class="skill-item">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg">
        <p>CSS</p>
      </div>

      <div class="skill-item">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg">
        <p>JavaScript</p>
      </div>

      <div class="skill-item">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg">
        <p>Python</p>
      </div>
    </div>
  </div>

  <!-- Sosmed -->
  <div class="card">
    <h2>🔗 Social Links</h2>

    <div class="socials">
      <a href="https://instagram.com/@andwisakti" target="_blank">Instagram</a>
      <a href="https://linktr.ee/andwisakti" target="_blank">Linktree</a>
      <a href="https://youtube.com/@andwisakti" target="_blank">YouTube</a>
    </div>
  </div>

</div>

<script>
/* --- PARTIKEL GENERATOR --- */
function createParticles() {
  const container = document.getElementById("particles");
  const count = 40;

  for (let i = 0; i < count; i++) {
    const p = document.createElement("div");
    p.classList.add("particle");

    const size = Math.random() * 4 + 2;
    p.style.width = size + "px";
    p.style.height = size + "px";

    p.style.left = Math.random() * 100 + "vw";
    p.style.animationDuration = (6 + Math.random() * 6) + "s";
    p.style.animationDelay = Math.random() * 5 + "s";

    container.appendChild(p);
  }
}

createParticles();
</script>

</body>
</html>
