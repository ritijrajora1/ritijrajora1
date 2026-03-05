
## 🌐 Socials:
[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/ritijrajora) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/ritij-rajora-9591a83ab) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:ritijrajora021@gmail.com) 

# 💻 Tech Stack:
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white) ![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=ritijrajora1&theme=dark&hide_border=false&include_all_commits=true&count_private=false)<br/>
![](https://nirzak-streak-stats.vercel.app/?user=ritijrajora1&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=ritijrajora1&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

<!DOCTYPE html>
<html>
<head>
  <title>Catch the Fruit Game</title>
  <style>
    body {
      background-color: #f0f8ff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }
    #game {
      width: 400px;
      height: 500px;
      border: 2px solid #333;
      position: relative;
      background-color: #cce7ff;
      overflow: hidden;
    }
    #basket {
      width: 80px;
      height: 20px;
      background-color: #ff6347;
      position: absolute;
      bottom: 10px;
      left: 160px;
      border-radius: 10px;
    }
    .fruit {
      width: 30px;
      height: 30px;
      background-color: #32cd32;
      border-radius: 50%;
      position: absolute;
      top: 0;
    }
    #score {
      position: absolute;
      top: 5px;
      left: 5px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div id="game">
    <div id="score">Score: 0</div>
    <div id="basket"></div>
  </div>

  <script>
    const basket = document.getElementById("basket");
    const game = document.getElementById("game");
    const scoreDisplay = document.getElementById("score");
    let score = 0;

    // Move basket
    document.addEventListener("keydown", (e) => {
      const left = parseInt(window.getComputedStyle(basket).left);
      if (e.key === "ArrowLeft" && left > 0) basket.style.left = left - 20 + "px";
      if (e.key === "ArrowRight" && left < game.offsetWidth - basket.offsetWidth)
        basket.style.left = left + 20 + "px";
    });

    // Create fruit
    function createFruit() {
      const fruit = document.createElement("div");
      fruit.classList.add("fruit");
      fruit.style.left = Math.floor(Math.random() * (game.offsetWidth - 30)) + "px";
      game.appendChild(fruit);

      let fruitFall = setInterval(() => {
        let top = parseInt(window.getComputedStyle(fruit).top);
        if (top > game.offsetHeight - 50) {
          let basketLeft = parseInt(window.getComputedStyle(basket).left);
          let fruitLeft = parseInt(fruit.style.left);
          if (fruitLeft + 30 > basketLeft && fruitLeft < basketLeft + 80) {
            score++;
            scoreDisplay.innerText = "Score: " + score;
          }
          fruit.remove();
          clearInterval(fruitFall);
        } else {
          fruit.style.top = top + 5 + "px";
        }
      }, 50);
    }

    // Generate fruits every 1 second
    setInterval(createFruit, 1000);
  </script>
</body>
</html>
<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
