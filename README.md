<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>پنل شناور</title>
  <style>
    body {
      font-family: sans-serif;
      margin: 0;
      padding: 0;
    }

    /* آیکون شناور */
    #toggleIcon {
      position: fixed;
      top: 20px;
      left: 20px;
      width: 50px;
      height: 50px;
      background-color: #0078D7;
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      z-index: 1000;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    }

    /* پنل کناری */
    #sidePanel {
      position: fixed;
      top: 0;
      left: -250px; /* مخفی باشه اول */
      width: 250px;
      height: 100%;
      background-color: #f1f1f1;
      box-shadow: 2px 0 5px rgba(0,0,0,0.2);
      padding: 20px;
      transition: left 0.3s ease;
      z-index: 999;
    }

    #sidePanel.open {
      left: 0;
    }
  </style>
</head>
<body>

  <!-- آیکون -->
  <div id="toggleIcon">📘</div>

  <!-- پنل کناری -->
  <div id="sidePanel">
    <h3>اسم من تورنتو است</h3>
  </div>

  <script>
    const icon = document.getElementById('toggleIcon');
    const panel = document.getElementById('sidePanel');

    icon.addEventListener('click', () => {
      panel.classList.toggle('open');
    });
  </script>

</body>
</html>
