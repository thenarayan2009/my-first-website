<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign Up and Sign In Page</title>
    <style>
        /* Default Light Theme */
        :root {
            --background-color: #a8edea;
            --text-color: #333;
            --container-bg: white;
            --button-bg: #4CAF50;
            --button-hover-bg: #45a049;
            --forgot-password-color: red;
            --sign-up-color: blue;
        }

        body {
            font-family: Arial, sans-serif;
            font-weight: bold;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: var(--background-color);
            color: var(--text-color);
            position: relative;
            transition: background-color 0.3s, color 0.3s;
        }

        .container {
            width: 300px;
            padding: 30px;
            background-color: var(--container-bg);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
            transition: background-color 0.3s;
        }

        .container img {
            width: 100%;
            height: auto;
            max-height: 300px;
            object-fit: cover;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .container h2 {
            margin-bottom: 20px;
            font-size: 24px;
        }

        .container input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }

        .container button {
            width: 100%;
            padding: 10px;
            border: none;
            background-color: var(--button-bg);
            color: white;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background-color 0.3s;
        }

        .container button:hover {
            background-color: var(--button-hover-bg);
        }

        /* Links below the form */
        .options {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            font-size: 14px;
        }

        .options .forgot-password {
            color: var(--forgot-password-color);
            text-decoration: underline;
        }

        .options .sign-up {
            color: var(--sign-up-color);
            text-decoration: underline;
        }

        .options .sign-up:hover {
            text-decoration: underline;
        }

        /* Three dots menu styles */
        .menu {
            position: absolute;
            top: 20px;
            right: 20px;
            cursor: pointer;
            font-size: 24px;
            color: var(--text-color);
        }

        .dropdown {
            display: none;
            position: absolute;
            right: 0;
            top: 40px;
            background-color: var(--container-bg);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            border-radius: 5px;
            width: 150px;
            z-index: 10;
            transition: background-color 0.3s;
        }

        .dropdown a {
            display: block;
            padding: 10px;
            color: var(--text-color);
            text-decoration: none;
            border-bottom: 1px solid #ccc;
        }

        .dropdown a:hover {
            background-color: #f1f1f1;
        }

        /* Show dropdown when menu is clicked */
        .menu.active + .dropdown {
            display: block;
        }
    </style>
</head>
<body>
    <div class="menu" onclick="toggleMenu()">&#x2022;&#x2022;&#x2022;</div>
    <div class="dropdown">
        <a href="https://myshopprime.com/Mahakal.fashion.collection/pbyvmnr">Shop</a>
        <a href="#">Home</a>
        <a href="#">Help</a>
    </div>

    <!-- Sign Up Page Container -->
    <div class="container" id="signupPage">
        <img src="https://your-image-link-here.jpg" alt="Sign Up Image">
        <h2>Sign Up</h2>
        <form action="/signup" method="post">
            <input type="text" name="username" placeholder="Username" required>
            <input type="email" name="email" placeholder="Email ID" required>
            <input type="password" name="password" placeholder="Password" required>
            <button type="submit">Sign Up</button>
        </form>
        
        <div class="options">
            <a href="#" class="forgot-password">Forgot Password?</a>
            <a href="#" class="sign-in" onclick="showSignIn()">Sign In</a>
        </div>
    </div>

    <!-- Sign In Page Container -->
    <div class="container" id="signinPage" style="display: none;">
        <img src="https://your-image-link-here.jpg" alt="Sign In Image">
        <h2>Sign In</h2>
        <form action="/signin" method="post">
            <input type="text" name="username" placeholder="Username or Email" required>
            <input type="password" name="password" placeholder="Password" required>
            <button type="submit">Sign In</button>
        </form>
        
        <div class="options">
            <a href="#" class="forgot-password">Forgot Password?</a>
            <a href="#" class="sign-up" onclick="showSignUp()">Sign Up</a>
        </div>
    </div>

    <script>
        // Toggle the menu visibility
        function toggleMenu() {
            document.querySelector('.menu').classList.toggle('active');
        }

        // Show the Sign In page and hide the Sign Up page
        function showSignIn() {
            document.getElementById('signupPage').style.display = 'none';
            document.getElementById('signinPage').style.display = 'block';
        }

        // Show the Sign Up page and hide the Sign In page
        function showSignUp() {
            document.getElementById('signinPage').style.display = 'none';
            document.getElementById('signupPage').style.display = 'block';
        }
    </script>
</body>
</html>p
