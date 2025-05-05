# Html-code-for-javascript-
<!DOCTYPE html>
<html>
<head>
  <title>Interactive Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 30px;
    }
    .success {
      color: green;
    }
    .error {
      color: red;
    }
    #output {
      margin-top: 20px;
    }
  </style>
</head>
<body>

  <h1>User Registration</h1>
  <form id="userForm">
    <label for="name">Name:</label><br>
    <input type="text" id="name" required><br><br>

    <label for="email">Email:</label><br>
    <input type="email" id="email" required><br><br>

    <button type="submit">Submit</button>
  </form>

  <div id="output"></div>

  <script>
    document.getElementById('userForm').addEventListener('submit', function(event) {
      event.preventDefault(); // Stop form from submitting

      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const output = document.getElementById('output');

      // Simple validation
      if (name === '' || email === '') {
        output.innerHTML = '<p class="error">Please fill in all fields.</p>';
        return;
      }

      if (!validateEmail(email)) {
        output.innerHTML = '<p class="error
        
