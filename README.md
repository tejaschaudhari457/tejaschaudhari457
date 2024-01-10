<!-- Add this to the top of your README.md file -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      transition: background-color 0.5s;
    }
    /* Add your light theme styles here */
    body.light {
      background-color: #ffffff;
      color: #000000;
    }
    /* Add your dark theme styles here */
    body.dark {
      background-color: #1a1a1a;
      color: #ffffff;
    }
    .toggle-container {
      display: flex;
      justify-content: space-between;
      margin: 10px 0;
    }
    .toggle-label {
      margin-right: 10px;
    }
  </style>
</head>
<body class="light">

<!-- Add your README content here -->

<!-- Add this toggle button at the end of your README.md file -->
<div class="toggle-container">
  <span class="toggle-label">Toggle theme:</span>
  <label class="switch">
    <input type="checkbox" id="themeToggle">
    <span class="slider round"></span>
  </label>
</div>

<script>
  const themeToggle = document.getElementById('themeToggle');
  const body = document.body;

  themeToggle.addEventListener('change', () => {
    body.classList.toggle('dark', themeToggle.checked);
    body.classList.toggle('light', !themeToggle.checked);
  });
</script>
</body>
</html>
