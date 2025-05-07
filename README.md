<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Línea Cambiante</title>
  <style>
    /* Estilo para la línea */
    .color-line {
      width: 100%;
      height: 10px; /* Altura de la línea */
      background-color: white; /* Color inicial */
      transition: background-color 0.5s ease; /* Transición suave */
    }
  </style>
</head>
<body>
  <!-- Línea que cambia de color -->
  <div class="color-line" id="colorLine"></div>

  <script>
    // Lista de colores a alternar
    const colors = ['white', 'black', 'gray'];
    let currentIndex = 0;

    // Función para cambiar el color
    function changeColor() {
      const line = document.getElementById('colorLine');
      currentIndex = (currentIndex + 1) % colors.length; // Alternar entre colores
      line.style.backgroundColor = colors[currentIndex];
    }

    // Cambiar color cada 1 segundo
    setInterval(changeColor, 1000);
  </script>
</body>
</html> 