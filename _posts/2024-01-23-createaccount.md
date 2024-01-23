<html>
<head>
  <script>
    var validUsernames = {};
    function checkPW() {
      var username = document.getElementById("username").value;
      var password = document.getElementById("password").value;
      var confirmPassword = document.getElementById("confirmPassword").value;
      if (password !== confirmPassword) {
        alert("Passwords do not match. Try again");
        return false;
      } 
      validUsernames[username] = password;
      console.log("Username: " + username + ", Password: " + password);
      return true;
    }
  </script>
</head>
<body>

<h2>Create Account Page</h2>

<form onsubmit="return checkPW()">
  <label for="username">Username:</label><br>
  <input type="text" id="username" name="username" required><br>
  <label for="password">Password:</label><br>
  <input type="password" id="password" name="password" required><br>
  <label for="confirmPassword">Confirm Password:</label><br>
  <input type="password" id="confirmPassword" name="confirmPassword" required><br>
  <input type="submit" value="Submit">
</form> 

</body>
</html>
