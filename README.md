<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>JARVIS Portfolio - Nalla Vijay Balaji</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Orbitron', sans-serif;
    }

    body {
      background: radial-gradient(circle at center, #0a0a0a, #000000);
      color: #ffffff;
      overflow-x: hidden;
    }

    .container {
      padding: 40px 20px;
      text-align: center;
    }

    h1 {
      font-size: 3rem;
      color: #ff2a2a;
      letter-spacing: 3px;
    }

    .subtitle {
      margin-top: 10px;
      color: #aaa;
    }

    .hud-box {
      border: 1px solid rgba(255, 0, 0, 0.4);
      padding: 20px;
      margin: 30px auto;
      max-width: 800px;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(255, 0, 0, 0.2);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .card {
      background: #111;
      padding: 20px;
      border-radius: 10px;
      border: 1px solid #222;
      transition: 0.3s;
    }

    .card:hover {
      transform: scale(1.05);
      border-color: red;
      box-shadow: 0 0 15px red;
    }

    .tag {
      display: inline-block;
      margin: 5px;
      padding: 5px 10px;
      border: 1px solid red;
      border-radius: 20px;
      font-size: 0.8rem;
    }

    .footer {
      margin-top: 50px;
      font-size: 0.9rem;
      color: #888;
    }

    .btn {
      display: inline-block;
      margin: 10px;
      padding: 10px 20px;
      border: 1px solid red;
      color: white;
      text-decoration: none;
      transition: 0.3s;
    }

    .btn:hover {
      background: red;
      box-shadow: 0 0 10px red;
    }

    .typing {
      margin-top: 15px;
      color: #ff4d4d;
      font-size: 1.2rem;
    }

  </style>
</head>

<body>

  <div class="container">

    <h1>JARVIS PROTOCOL</h1>
    <p class="subtitle">Nalla Vijay Balaji | AI Engineer</p>
    <p class="typing" id="typing"></p>

    <div class="hud-box">
      <p>⚙️ SYSTEM STATUS: ONLINE</p>
      <p>🧠 CORE: AI / LLM / MULTI-AGENT</p>
      <p>⚡ POWER: 100%</p>
    </div>

    <div class="grid">

      <div class="card">
        <h3>🧠 AI Core</h3>
        <p>LLMs, RAG, Multi-Agent Systems, Computer Vision</p>
      </div>

      <div class="card">
        <h3>⚡ Languages</h3>
        <p>Python, C++, Java, JavaScript</p>
      </div>

      <div class="card">
        <h3>🌐 Web & DB</h3>
        <p>HTML, CSS, MongoDB, Linux</p>
      </div>

      <div class="card">
        <h3>🎓 Education</h3>
        <p>B.Tech CSE — CGPA 8.65</p>
      </div>

    </div>

    <div class="hud-box">
      <h2>🧪 Projects</h2>
      <p><b>NEXTAURA</b> → AI Copilot (+30% speed)</p>
      <p><b>IEEE Website</b> → 40% faster load</p>
    </div>

    <div class="hud-box">
      <h2>🏆 Achievements</h2>
      <p>🥈 InnoQuest #3</p>
      <p>🏅 Top 5 InnoQuest #1</p>
      <p>🥈 Runner-Up Parse-a-thon</p>
      <p>✅ Smart India Hackathon 2025</p>
    </div>

    <div class="hud-box">
      <h2>📡 Skills</h2>
      <span class="tag">Leadership</span>
      <span class="tag">Communication</span>
      <span class="tag">Teamwork</span>
      <span class="tag">Problem Solving</span>
    </div>

    <div>
      <a href="https://linkedin.com" class="btn">LinkedIn</a>
      <a href="mailto:nallavijaibalaji@gmail.com" class="btn">Email</a>
    </div>

    <div class="footer">
      <p>"If you're nothing without the code, then you shouldn't have it."</p>
    </div>

  </div>

  <script>
    const text = [
      "Initializing JARVIS...",
      "Deploying AI Systems...",
      "Building the Future...",
      "System Ready 🚀"
    ];

    let i = 0, j = 0;
    let current = "";
    let isDeleting = false;

    function type() {
      const element = document.getElementById("typing");

      if (i < text.length) {
        if (!isDeleting && j <= text[i].length) {
          current = text[i].substring(0, j++);
        } else if (isDeleting && j >= 0) {
          current = text[i].substring(0, j--);
        }

        element.textContent = current;

        if (j === text[i].length) isDeleting = true;
        if (j === 0 && isDeleting) {
          isDeleting = false;
          i++;
        }
      } else {
        i = 0;
      }

      setTimeout(type, isDeleting ? 50 : 100);
    }

    type();
  </script>

</body>
</html>
