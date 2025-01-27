<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Random Spy Name Generator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background-color: white;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      padding: 30px;
      text-align: center;
      max-width: 400px;
      width: 100%;
    }

    h1 {
      font-size: 24px;
      margin-bottom: 20px;
    }

    .spy-name {
      font-size: 28px;
      font-weight: bold;
      color: #4CAF50;
      margin: 20px 0;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>Spy Name Generator</h1>
  <div class="spy-name" id="spy-name">Your Spy Name</div>
  <button onclick="generateSpyName()">Generate Spy Name</button>
</div>

<script>
  // Arrays of spy name components
  const firstNames = ["Tommy"];
  const lastNames = ["Queue"];
  const codenames = ["Sam Handwiches"];

  // Function to generate a random spy name
  function generateSpyName() {
    const firstName = firstNames[Math.floor(Math.random() * firstNames.length)];
    const lastName = lastNames[Math.floor(Math.random() * lastNames.length)];
    const codename = codenames[Math.floor(Math.random() * codenames.length)];

    // Display the generated spy name
    document.getElementById("spy-name").textContent = `${firstName} "${codename}" ${lastName}`;
  }
</script>

</body>
</html>
