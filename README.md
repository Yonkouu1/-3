<!DOCTYPE html>
<html>
<head>
  <title>Basit Site</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      padding-top: 50px;
    }
    h1 {
      color: #333;
    }
    img {
      width: 200px;
      transition: all 0.5s ease;
    }
    button {
      margin: 20px;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
    }
    #wrongButton {
      background-color: #ff4d4d;
      color: white;
    }
    #rightButton {
      background-color: #4CAF50;
      color: white;
    }
  </style>
</head>
<body>

  <h1>Doğru butonu bul!</h1>
  <img id="myGif" src="https://media.giphy.com/media/l0HlBO7eyXzSZkJri/giphy.gif" alt="GIF">
  <br>
  <button id="wrongButton">Yanlış</button>
  <button id="rightButton">Doğru</button>

  <script>
    let stage = 0;
    const gif = document.getElementById("myGif");
    const wrongBtn = document.getElementById("wrongButton");

    wrongBtn.addEventListener("click", function() {
      stage++;
      if (stage === 1) {
        gif.style.width = "300px";
      } else if (stage === 2) {
        gif.style.width = "400px";
      } else if (stage === 3) {
        gif.style.width = "500px";
      } else if (stage === 4) {
        wrongBtn.style.display = "none";
      }
    });
  </script>

</body>
</html>
