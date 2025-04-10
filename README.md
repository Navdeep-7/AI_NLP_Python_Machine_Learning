<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Machine Learning Predictor</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f2f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .container {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
      text-align: center;
      width: 300px;
    }

    input[type="number"] {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
    }

    button {
      padding: 10px 20px;
      border: none;
      background-color: #4CAF50;
      color: white;
      border-radius: 8px;
      cursor: pointer;
    }

    #result {
      margin-top: 20px;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>House Price Predictor</h2>
    <input type="number" id="sizeInput" placeholder="Enter size (sq ft)" />
    <button onclick="predictPrice()">Predict</button>
    <div id="result"></div>
  </div>

  <script>
    function predictPrice() {
      const size = document.getElementById("sizeInput").value;
      if (!size) {
        alert("Please enter a value.");
        return;
      }

      // Simulate prediction (replace this with actual API call)
      const predictedPrice = 100 * size + 50000; // Dummy formula
      document.getElementById("result").innerText = "Predicted Price: $" + predictedPrice.toLocaleString();
    }
  </script>
</body>
</html>
