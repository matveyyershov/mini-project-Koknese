# mini-project-Koknese
![11](https://github.com/user-attachments/assets/8868adde-eaef-47c2-b8f0-9e38005db6fa)
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Кокнесе</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
    }

    header {
      text-align: center;
      background-color: #4CAF50;
      color: white;
      padding: 20px;
    }

    #map, #history, #images {
      padding: 20px;
    }

    h2 {
      color: #333;
    }

    #map-container {
      height: 400px;
      width: 100%;
    }

    img {
      margin: 10px;
      border-radius: 8px;
    }

    footer {
      text-align: center;
      background-color: #333;
      color: white;
      padding: 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Добро пожаловать в Кокнесе!</h1>
  </header>

  <section id="map">
    <h2>Карта города</h2>
    <div id="map-container"></div>
  </section>

  <section id="history">
    <h2>История города</h2>
    <p>Кокнесе — это город с богатой историей. Он был основан в XIII веке, а сегодня представляет собой важный культурный центр Латвии.</p>
  </section>

  <section id="images">
    <h2>Картинки города</h2>
    <img src="koknese1.jpg" alt="Кокнесе 1" width="300">
    <img src="koknese2.jpg" alt="Кокнесе 2" width="300">
  </section>

  <footer>
    <p>&copy; 2024, Кокнесе</p>
  </footer>

  <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
  <script>
    // Инициализация карты
    var map = L.map('map-container').setView([56.5026, 26.0916], 13); // Координаты Кокнесе

    // Добавление тайлсета
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(map);

    // Добавление маркера на карту
    L.marker([56.5026, 26.0916]).addTo(map)
      .bindPopup('<b>Кокнесе</b><br>Город в Латвии')
      .openPopup();
  </script>
</body>
</html>
