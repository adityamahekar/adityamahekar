<!-- Galactic-themed GitHub Profile -->Add commentMore actions
<h1 align="left">Hey 👋 What's up?</h1>

<div align="center" style="background: url('https://source.unsplash.com/featured/?galaxy,stars'); background-size: cover; padding: 20px; border-radius: 15px;">
  <h1 style="color: #fff; font-size: 36px;">👋 Hi, I'm Aditya Mahekar</h1>
  <p style="color: #ddd; font-size: 18px;">Java | C | Python | Front-End & Back-End Development | React.js | Databases</p>
</div>
---
<div align="right">
  <img height="150" src="https://i.postimg.cc/MZNc6rc8/download-removebg-preview.png"  />
</div>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Snake with Green Variant Food</title>
  <style>
    body {
      background: #0d1117;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(50, 15px);
      grid-template-rows: repeat(7, 15px);
      gap: 3px;
    }

    .cell {
      width: 15px;
      height: 15px;
      background: #161b22;
      border-radius: 2px;
      transition: all 0.1s ease;
    }

    .snake {
      background-color: #6a0dad !important; /* Dark purple */
    }

    .snake-head {
      background-color: #b266ff !important; /* Light purple */
      transform: scale(1.4);
      border-radius: 4px;
    }

    .food-1 {
      background-color: #a8ffb3 !important; /* lightest green */
    }

    .food-2 {
      background-color: #6fff8e !important;
    }

    .food-3 {
      background-color: #2ecc71 !important;
    }

    .food-4 {
      background-color: #1e8449 !important; /* darkest green */
    }
  </style>
</head>
<body>
  <div class="grid" id="grid"></div>

  <script>
    const cols = 50;
    const rows = 7;
    const totalCells = cols * rows;
    const grid = document.getElementById('grid');

    const cells = [];
    for (let i = 0; i < totalCells; i++) {
      const cell = document.createElement('div');
      cell.classList.add('cell');
      grid.appendChild(cell);
      cells.push(cell);
    }

    let snake = [Math.floor(totalCells / 2)];
    const snakeLength = 4;
    let food = [];
    const maxFood = 100;
    const foodVariants = ['food-1', 'food-2', 'food-3', 'food-4'];

    function placeFood() {
      while (food.length < maxFood) {
        const newFood = Math.floor(Math.random() * totalCells);
        if (!food.some(f => f.index === newFood) && !snake.includes(newFood)) {
          const type = foodVariants[Math.floor(Math.random() * foodVariants.length)];
          food.push({ index: newFood, type });
        }
      }
    }

    function getXY(index) {
      return [index % cols, Math.floor(index / cols)];
    }

    function getIndex(x, y) {
      return y * cols + x;
    }

    function moveSnake() {
      const head = snake[0];
      const [hx, hy] = getXY(head);

      let target = food[0]?.index;
      let minDist = Infinity;
      for (const f of food) {
        const [fx, fy] = getXY(f.index);
        const dist = Math.abs(fx - hx) + Math.abs(fy - hy);
        if (dist < minDist) {
          minDist = dist;
          target = f.index;
        }
      }

      const [tx, ty] = getXY(target);
      let nx = hx;
      let ny = hy;

      if (hx < tx) nx++;
      else if (hx > tx) nx--;
      else if (hy < ty) ny++;
      else if (hy > ty) ny--;

      nx = Math.max(0, Math.min(cols - 1, nx));
      ny = Math.max(0, Math.min(rows - 1, ny));

      const newHead = getIndex(nx, ny);
      snake.unshift(newHead);

      const eatenIndex = food.findIndex(f => f.index === newHead);
      if (eatenIndex !== -1) {
        food.splice(eatenIndex, 1);
      }

      while (snake.length > snakeLength) {
        snake.pop();
      }
    }

    function render() {
      cells.forEach(cell => cell.className = 'cell');

      food.forEach(f => cells[f.index].classList.add(f.type));

      for (let i = 0; i < snake.length; i++) {
        const className = i === 0 ? 'snake-head' : 'snake';
        cells[snake[i]].classList.add(className);
      }
    }

    placeFood();
    render();

    setInterval(() => {
      moveSnake();
      placeFood();
      render();
    }, 120);
  </script>
</body>
</html>

  <!-- LinkedIn -->
  <p style="font-size: 18px; margin: 15px 0;">
    <strong>Connect with me:</strong> 
    <a href="https://www.linkedin.com/in/aditya-mahekar" target="_blank" style="color: #ffcc00; text-decoration: none; font-weight: bold;">LinkedIn</a>
---
<div align="center">
  <img src="https://profile-counter.glitch.me/adityamahekar/count.svg" alt="Profile counter" />
</div>
###

<h2 align="left">👋 Hi, I'm Aditya Mahekar</h2>

###



🛠️ Skills
###

<div align="center">
  <!-- Front-End -->
  <h3>Front-End Development</h3>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="HTML5" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="CSS3" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="JavaScript" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" height="40" alt="Bootstrap" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-original.svg" height="40" alt="jQuery" />

  <!-- Back-End -->
  <h3>Back-End Development</h3>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="40" alt="Node.js" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg" height="40" alt="Express.js" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="40" alt="Python" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="40" alt="Java" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="C" />

  <!-- Databases -->
  <h3>Databases</h3>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" height="40" alt="MongoDB" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" height="40" alt="PostgreSQL" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="40" alt="MySQL" />

  <!-- Tools -->
  <h3>Tools & Platforms</h3>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="40" alt="Git" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" height="40" alt="Linux" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" alt="VSCode" />
  <img height="200" src="https://i.postimg.cc/MZNc6rc8/download-removebg-preview.png"  />
</div>

---
### 🐍 Snake Animation
###
<div class="section">
   <p><strong style="margin-left:284px">Connect with me:</strong> <a href="https://www.linkedin.com/in/aditya-mahekar" target="_blank">LinkedIn</a></p>
   
  </div>


<div align="center">
  <img src="https://github.com/adityamahekar/adityamahekar/raw/output/snake.svg" alt="Snake animation" />
  <img src="https://profile-counter.glitch.me/adityamahekar/count.svg?"  />
</div>

---
<div align="center" style="
  background: url('https://images.unsplash.com/photo-1581349481447-938cb11162c4?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  padding: 20px;
  border-radius: 15px;
  color: white;
">
###

<img src="https://raw.githubusercontent.com/adityamahekar/adityamahekar/output/snake.svg" alt="Snake animation" />

###

  <!-- GitHub Stats -->
  <div style="margin: 20px;">
    <img src="https://github-readme-stats.vercel.app/api?username=adityamahekar&show_icons=true&theme=radical" height="150" alt="GitHub Stats" />
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=adityamahekar&layout=compact&theme=radical" height="150" alt="Top Languages" />
  </div>
  
  <!-- Streak Stats -->
  <div style="margin: 20px;">
    <img src="https://streak-stats.demolab.com?user=adityamahekar&theme=radical" height="150" alt="GitHub Streak Stats" />
  </div>
  Add commentMore actions
  <!-- Trophies -->
  <div style="margin: 20px;">
    <img src="https://github-profile-trophy.vercel.app/?username=adityamahekar&theme=radical" height="150" alt="GitHub Trophies" />
  </div>

  <!-- Snake Animation -->
  <div align="center" style="margin: 20px;">
    <img src="https://raw.githubusercontent.com/adityamahekar/adityamahekar/output/snake.svg" alt="Snake animation" />
  </div>

<br clear="both">

<div align="center">
  <img src="https://github-profile-trophy.vercel.app?username=adityamahekar&theme=radical&column=-1&row=1&margin-w=8&margin-h=8&no-bg=false&no-frame=false&order=4" height="150" alt="trophy graph"  />
  <img src="https://streak-stats.demolab.com?user=adityamahekar&locale=en&mode=daily&theme=dark&hide_border=false&border_radius=5&order=3" height="145" alt="streak graph"  />
  <img src="https://github-readme-stats.vercel.app/api?username=adityamahekar&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=radical&locale=en&hide_border=false&order=1" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=adityamahekar&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=10&theme=radical&hide_border=false&order=2" height="200" alt="languages graph"  />
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=adityamahekar&radius=16&theme=redical&area=true&order=5" height="300" alt="activity-graph graph"  />
</div>

###
