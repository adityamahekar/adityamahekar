<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Aditya Mahekar - Portfolio</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: url('https://source.unsplash.com/featured/?galaxy,stars') no-repeat center center fixed;
      background-size: cover;
      color: white;
    }

    .container {
      padding: 40px;
      backdrop-filter: blur(8px);
      background: rgba(0, 0, 0, 0.6);
      border-radius: 15px;
      margin: 40px auto;
      max-width: 1000px;
      box-shadow: 0 0 30px rgba(0, 255, 255, 0.4);
    }

    .glow-text {
      text-align: center;
      font-size: 36px;
      color: #fff;
      text-shadow: 0 0 10px #0ff, 0 0 20px #0ff, 0 0 30px #0ff;
    }

    .sub-text {
      text-align: center;
      font-size: 18px;
      color: #ccc;
      margin-bottom: 20px;
    }

    .profile-img {
      display: block;
      margin: 0 auto 30px;
      height: 150px;
    }

    .section {
      margin-top: 40px;
    }

    .section h2 {
      color: #00ffe0;
      text-shadow: 0 0 5px #00ffc8;
      border-bottom: 1px solid #00ffc8;
      padding-bottom: 5px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(50, 15px);
      grid-template-rows: repeat(7, 15px);
      gap: 3px;
      margin-top: 20px;
    }

    .cell {
      width: 15px;
      height: 15px;
      background: #161b22;
      border-radius: 2px;
    }

    .snake { background-color: #6a0dad !important; }
    .snake-head { background-color: #b266ff !important; transform: scale(1.4); border-radius: 4px; }
    .food-1 { background-color: #a8ffb3 !important; }
    .food-2 { background-color: #6fff8e !important; }
    .food-3 { background-color: #2ecc71 !important; }
    .food-4 { background-color: #1e8449 !important; }

    .footer {
      text-align: center;
      padding: 20px;
      font-size: 14px;
      color: #999;
    }

    a {
      color: #00ffe0;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <div class="container">
    <img src="https://i.postimg.cc/MZNc6rc8/download-removebg-preview.png" alt="Aditya" class="profile-img" />
    <h1 class="glow-text">👋 Hi, I'm Aditya Mahekar</h1>
    <p class="sub-text">Java | C | Python | Front-End & Back-End Development | React.js | Databases</p>

    <div class="section">
      <h2>💻 Tech Stack</h2>
      <ul>
        <li>Languages: Java, C, Python</li>
        <li>Frontend: HTML, CSS, JavaScript, React.js</li>
        <li>Backend: Node.js, Express</li>
        <li>Databases: MongoDB, MySQL</li>
        <li>Tools: Git, GitHub, Netlify</li>
      </ul>
    </div>

    <div class="section">
      <h2>🎮 Snake Game Visual Grid</h2>
      <div class="grid" id="grid"></div>
    </div>

    <div class="section">
      <h2>📫 Contact</h2>
      <p>Email: <a href="mailto:adityamahekar1234@gmail.com">adityamahekar1234@gmail.com</a></p>
      <p>GitHub: <a href="https://github.com/AdityaMahekar" target="_blank">AdityaMahekar</a></p>
      <p>LinkedIn: <a href="#" target="_blank">Your LinkedIn</a></p>
    </div>
  </div>

  <div class="footer">
    🚀 Made with 💙 by Aditya Mahekar
  </div>

  <script>
    // Grid Generator
    const grid = document.getElementById("grid");
    for (let i = 0; i < 50 * 7; i++) {
      const cell = document.createElement("div");
      cell.classList.add("cell");

      // Randomly color some cells for snake/food effect
      const r = Math.random();
      if (r < 0.02) cell.classList.add("snake-head");
      else if (r < 0.06) cell.classList.add("snake");
      else if (r < 0.10) cell.classList.add("food-1");
      else if (r < 0.13) cell.classList.add("food-2");
      else if (r < 0.15) cell.classList.add("food-3");
      else if (r < 0.16) cell.classList.add("food-4");

      grid.appendChild(cell);
    }
  </script>
</body>
</html>
