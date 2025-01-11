<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Landing Page</title>
  <style>
    /* General styles */
    body {
      margin: 0;
      padding: 0;
      font-family: 'Helvetica Neue', sans-serif;
      background-color: #DBE4E2;
    }

    .LandingPage {
      width: 393px;
      height: 700px;
      position: relative;
      background: #ffffff;
      margin: auto;
      padding: 20px;
    }

    .TravelBanner12 {
      width: 492.81px;
      height: 79px;
      position: absolute;
      top: 69px;
      left: 0px;
    }

    .TravellerInTerminal1 {
      width: 184px;
      height: 284px;
      position: absolute;
      top: 220px;
      left: 207px;
      box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    }

    .input-group {
      position: absolute;
      width: 223px;
      margin-bottom: 20px;
    }

    label {
      font-size: 14px;
      color: #868686;
      display: block;
      margin-bottom: 5px;
    }

    input[type="text"], input[type="password"] {
      width: 90%;
      padding: 5px;
      font-size: 15px;
      border: 0px solid #B7B7B7;
      border-radius: 4px;
    }

    .toggle-password {
      font-size: 12px;
      color: #174B98;
      cursor: pointer;
      margin-top: 5px;
      display: inline-block;
    }

    .UsernameAlias-group {
      top: 216px;
      left: 30px;
    }

    .Password-group {
      top: 274px;
      left: 30px;
    }

    .ForgotPassword-group {
      top: 405px;
      left: 30px;
    }

    .ForgotPassword-group a {
      color: #174B98;
      font-size: 15px;
      text-decoration: none;
      cursor: pointer;
    }

    .ReistellLogo {
      width: 40px;
      height: 42px;
      position: absolute;
      top: 21px;
      left: 314px;
    }

    /* Create Account Button */
    .create-account-btn {
      position: absolute;
      top: 500px;
      left: 30px;
      width: 150px;
      padding: 10px;
      font-size: 16px;
      font-weight: bold;
      text-align: center;
      color: white;
      background-color: #B00C16;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease, transform 0.2s ease;
    }

    .create-account-btn:hover {
      background-color: #B00C16;
      transform: scale(1.05);
    }

    .create-account-btn:active {
      transform: scale(1.1);
    }
  </style>
</head>
<body>
  <div class="LandingPage">
    <img class="TravelBanner12" src="https://reistell.com/wp-content/uploads/2025/01/Travel-banner-1-1-e1736414689664.png" alt="Travel Banner">
    <img class="TravellerInTerminal1" src="https://reistell.com/wp-content/uploads/2024/08/Traveller-In-Terminal-e1736414528623.png" alt="Traveller In Terminal">
    
   <form action="login.php" method="POST">
  <div class="input-group UsernameAlias-group">
    <label for="usernameAlias">Username / Alias</label>
    <input type="text" id="usernameAlias" name="usernameAlias" placeholder="Enter your username" required>
  </div>

  <div class="input-group Password-group">
    <label for="password">Password</label>
    <input type="password" id="password" name="password" placeholder="Enter your password" required>
    <span class="toggle-password" onclick="togglePassword()">Show Password</span>
  </div>

  <button type="submit" class="create-account-btn">Login</button>
</form>

    <!-- Forgot Password Link -->
    <div class="input-group ForgotPassword-group">
      <label for="forgotPassword">Forgot Password?</label>
      <a href="#" id="forgotPassword" onclick="resetFields()">Click here to reset</a>
    </div>

    <img class="ReistellLogo" src="https://reistell.com/wp-content/uploads/2022/05/Reistell_logo-01.png" alt="Reistell Logo">
    
    <!-- Create Account Button -->
    <a href="https://reistell.com/to-subscribe" class="create-account-btn">Create Account</a>
  </div>

  <script>
    function togglePassword() {
      const passwordField = document.getElementById('password');
      const toggleText = document.querySelector('.toggle-password');
      
      if (passwordField.type === 'password') {
        passwordField.type = 'text';
        toggleText.textContent = 'Hide Password';
      } else {
        passwordField.type = 'password';
        toggleText.textContent = 'Show Password';
      }
    }

    function resetFields() {
      document.getElementById('usernameAlias').value = '';
      document.getElementById('password').value = '';
      alert('Fields have been reset.');
    }
  </script>
</body>
</html>
