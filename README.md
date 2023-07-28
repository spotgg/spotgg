<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Preloader Example</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    .preloader-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #f8f8f8;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
    }

    .preloader {
      border: 6px solid #3498db;
      border-top: 6px solid transparent;
      border-radius: 50%;
      width: 50px;
      height: 50px;
      animation: spin 1.5s linear infinite;
    }

    @keyframes spin {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    /* Hide the preloader when content is loaded */
    body.loaded .preloader-container {
      display: none;
    }
  </style>
</head>
<body>
  <div class="preloader-container">
    <div class="preloader"></div>
  </div>

  <!-- Your website content goes here -->
  <h1>Hello, this is my website!</h1>
  <p>Welcome to my awesome website!</p>

  <script>
    // JavaScript to remove preloader when content is loaded
    window.addEventListener('load', function () {
      document.body.classList.add('loaded');
    });
  </script>
</body>
</html>
