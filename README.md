<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine ❤️</title>
  <style>
    body {
      height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      font-family: Arial, sans-serif;
      text-align: center;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    h1 {
      margin-bottom: 30px;
      color: #e91e63;
    }

    .buttons {
      display: flex;
      gap: 20px;
      justify-content: center;
      align-items: center;
    }

    button {
      border: none;
      padding: 15px 30px;
      font-size: 20px;
      border-radius: 12px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    #yesBtn {
      background-color: #4caf50;
      color: white;
      font-size: 22px;
    }

    #noBtn {
      background-color: #f44336;
      color: white;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Will you be my Valentine? 💖</h1>
    <div class="buttons">
      <button id="yesBtn">Yes 😍</button>
      <button id="noBtn">No 😢</button>
    </div>
  </div>

  <script>
    let yesSize = 22;
    let noScale = 1;

    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");

    noBtn.addEventListener("click", () => {
      // make YES bigger
      yesSize += 10;
      yesBtn.style.fontSize = yesSize + "px";
      yesBtn.style.padding = "20px " + (yesSize + 20) + "px";

      // make NO smaller
      noScale -= 0.2;
      noBtn.style.transform = `scale(${noScale})`;

      // hide NO if too small
      if (noScale <= 0.2) {
        noBtn.style.display = "none";
      }
    });

    yesBtn.addEventListener("click", () => {
      document.body.innerHTML = `
        <div style="
          height:100vh;
          display:flex;
          justify-content:center;
          align-items:center;
          background:linear-gradient(135deg,#ff9a9e,#fad0c4);
          font-family:Arial;
          text-align:center;
        ">
          <h1 style="color:#e91e63;font-size:50px;">
            Yayyy 💕<br>
            Happy Valentine’s Day 😘
          </h1>
        </div>
      `;
    });
  </script>

</body>
</html>
