<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Línea Cambiante</title>
  <style>
    .color-line {
      width: 100%;
      height: 10px; 
      background-color: white; 
      transition: background-color 0.5s ease; 
    }
  </style>
</head>
<body>
  <!-- Línea que cambia de color -->
  <div class="color-line" id="colorLine"></div>

  <script>
    const colors = ['white', 'black', 'gray'];
    let currentIndex = 0;

   
    function changeColor() {
      const line = document.getElementById('colorLine');
      currentIndex = (currentIndex + 1) % colors.length; 
      line.style.backgroundColor = colors[currentIndex];
    }

    setInterval(changeColor, 1000);
  </script>
</body>
</html> 