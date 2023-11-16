<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>For Hanri</title>
    <style>
      body {
        margin: 0;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100vh;
        background-color: black;
        animation: twinkling 5s infinite;
        color: white;
      }

      @keyframes twinkling {
        0% {
          background-position: 0 0;
        }

        100% {
          background-position: 100% 100%;
        }
      }

      .stars {
        position: absolute;
        width: 1px;
        height: 1px;
        background: white;
        animation: twinkle 1s infinite;
      }

      @keyframes twinkle {
        0% {
          opacity: 1;
        }

        50% {
          opacity: 0.5;
        }

        100% {
          opacity: 1;
        }
      }

      h1 {
        color: yellow;
        text-align: center;
        margin: 20px 0;
      }

      .content {
        max-width: 800px;
        text-align: center;
        margin: 20px;
      }

      .playlist {
        margin-top: 20px;
      }

      .poem {
        margin-top: 20px;
      }

      .counter {
        margin-top: 20px;
      }

      .gallery {
        margin-top: 20px;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
      }

      .gallery img {
        max-width: 100%;
        height: auto;
        margin: 10px;
      }
    </style>
  </head>
  <body>
    <h1 color="yellow">happy 6 months babe!</h1>
    <div class="poem">
      <h2>Dear Liefie Lyfie</h2>
      <p font="Fantasy">Who would've thought, we would end up together.The girl who walked into Mrs D Du Toits math class, blond hair, big ass school bag and PT clothes. Thank you for always being there for me no matter what. You have really changed me, making me happier than ever. There's this word in arabic "نور" which means nur or light. You're this unexplainable bundle of joy with nur all over you face. Happy 6 months babe i love you. I promise that I'll marry you one day. <br>
        <br>Love <br>
        <br>Your one and only husband Amier <br>
      </p>
    </div>
    <div class="counter">
      <h2>Days Since We've Been Together</h2>
      <p id="daysCounter"></p>
    </div>
    <div class="gallery">
      <h2>Memories Together</h2>
      <!-- Add your pictures here -->
      <img src="image1.jpg" alt="Us 1">
      <img src="image2.jpg" alt="Us 2">
      <img src="image1.jpg" alt="Us 3">
      <img src="image2.jpg" alt="Us 4">
      <img src="image1.jpg" alt="Us 5">
      <img src="image2.jpg" alt="Us 6">
      <img src="image2.jpg" alt="Us 7">
      <!-- Add more images as needed -->
    </div>
    </div>
    <script>
      document.addEventListener('DOMContentLoaded', function() {
        const numberOfStars = 100;
        for (let i = 0; i < numberOfStars; i++) {
          createStar();
        }

        function createStar() {
          const star = document.createElement('div');
          star.className = 'stars';
          // Set random position on the screen
          const posX = Math.random() * window.innerWidth;
          const posY = Math.random() * window.innerHeight;
          star.style.left = posX + 'px';
          star.style.top = posY + 'px';
          document.body.appendChild(star);
        }
        // Set the date you started the relationship
        const startDate = new Date('2023-05-20');
        updateDaysCounter(startDate);

        function updateDaysCounter(startDate) {
          const currentDate = new Date();
          const daysDiff = Math.floor((currentDate - startDate) / (1000 * 60 * 60 * 24));
          document.getElementById('daysCounter').innerText = daysDiff + ' days';
        }
      });
    </script>
  </body>
</html>
