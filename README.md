<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Signup Flow</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .signup-container {
            background: #ffffff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            width: 100%;
        }
        .signup-container h2 {
            margin-bottom: 20px;
            color: #333;
            text-align: center;
        }
        .signup-container label {
            display: block;
            margin-bottom: 8px;
            color: #555;
        }
        .signup-container input {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
        }
        .signup-container button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }
        .signup-container button:hover {
            background-color: #45a049;
        }
        .error {
            color: red;
            font-size: 12px;
        }
    </style>
</head>
<body>
    <div class="signup-container">
        <h2>Signup</h2>
        <form id="signupForm">
            <label for="name">Full Name:</label>
            <input type="text" id="name" name="name" placeholder="Enter your name" required>

            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" placeholder="Enter your email" required>

            <label for="password">Password:</label>
            <input type="password" id="password" name="password" placeholder="Enter a secure password" required>

            <label for="location">Location:</label>
            <input type="text" id="location" name="location" placeholder="Enter your location" required>

            <button type="submit">Sign Up</button>
        </form>
        <div id="error" class="error"></div>
    </div>

    <script>
        const form = document.getElementById('signupForm');
        const errorDiv = document.getElementById('error');

        form.addEventListener('submit', function(event) {
            event.preventDefault();
            errorDiv.textContent = '';

            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;

            if (password.length < 8) {
                errorDiv.textContent = 'Password must be at least 8 characters long.';
                return;
            }

            // Simulate a successful signup process
            alert(`Thank you for signing up, ${name}!`);
            form.reset();
        });
    </script>
</body>
</html>
