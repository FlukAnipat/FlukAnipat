<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Animated Developer Stack</title>
  <style>
    body {
      background: #0f172a;
      color: #f1f5f9;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 2rem;
      overflow-x: hidden;
    }

    h1, h2 {
      text-align: center;
      margin-bottom: 1rem;
      color: #38bdf8;
    }

    .icon-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(80px, 1fr));
      gap: 2rem;
      max-width: 800px;
      margin-top: 1rem;
    }

    .icon {
      width: 64px;
      height: 64px;
      transition: transform 0.4s ease, filter 0.4s ease;
      filter: drop-shadow(0 0 10px #0ea5e9);
    }

    .icon:hover {
      transform: scale(1.2) rotate(5deg);
      filter: drop-shadow(0 0 15px #38bdf8);
    }

    .label {
      text-align: center;
      margin-top: 0.5rem;
      font-size: 0.85rem;
      color: #cbd5e1;
    }

    .icon-block {
      display: flex;
      flex-direction: column;
      align-items: center;
      animation: float 4s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>
  <h1>🚀 Anipat Jaiworn</h1>
  <h2>My Tech Stack</h2>
  <div class="icon-grid">
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" alt="C" />
      <div class="label">C</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" alt="C#" />
      <div class="label">C#</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java" />
      <div class="label">Java</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" alt="Python" />
      <div class="label">Python</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="JavaScript" />
      <div class="label">JavaScript</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" alt="HTML5" />
      <div class="label">HTML5</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" alt="CSS3" />
      <div class="label">CSS3</div>
    </div>
    <div class="icon-block">
      <img class="icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" alt="React" />
      <div class="label">React</div>
    </div>
  </div>
</body>
</html>
