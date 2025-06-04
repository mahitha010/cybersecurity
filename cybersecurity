# cybersecurity
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Password Strength Checker</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 2rem;
      background-color: #f0f0f0;
    }
    input, button {
      padding: 0.5rem;
      font-size: 1rem;
      margin-right: 0.5rem;
    }
    #strength-output {
      margin-top: 1rem;
      padding: 1rem;
      border-radius: 4px;
      border: 1px solid #ccc;
      background-color: #fff;
      white-space: pre-wrap;
      word-break: break-word;
    }
  </style>
  <script>
    function checkPasswordStrength(password) {
      let strength = 0;
      if (password.length >= 8) strength += 1;
      if (/[a-z]/.test(password)) strength += 1;
      if (/[A-Z]/.test(password)) strength += 1;
      if (/\d/.test(password)) strength += 1;
      if (/[\W_]/.test(password)) strength += 1;

      const messages = [
        "Very Weak 🔴",
        "Weak 🟠",
        "Moderate 🟡",
        "Strong 🟢",
        "Very Strong 🔵"
      ];

      return messages[strength - 1] || "Too Short ❌";
    }

    function handlePasswordInput() {
      const password = document.getElementById('password-input').value;
      const strength = checkPasswordStrength(password);
      const outputDiv = document.getElementById('strength-output');
      
      outputDiv.textContent = "Password Strength: " + strength;
    }
  </script>
</head>
<body>
  <h1>Password Strength Checker</h1>
  <p>Enter a password to evaluate its strength based on common security criteria.</p>
  <input type="password" id="password-input" placeholder="Enter your password" size="50" />
  <button onclick="handlePasswordInput()">Check Strength</button>

  <div id="strength-output"></div>
</body>
</html>
