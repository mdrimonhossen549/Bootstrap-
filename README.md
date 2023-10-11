<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
    <style>
    body {
    font-family: Arial, sans-serif;
    background-color: #f2f2f2;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    background-color: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    max-width: 300px;
    text-align: center;
}

h2 {
    margin-top: 0;
}

input {
    width: 100%;
    margin: 10px 0;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    width: 100%;
    padding: 10px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

.hidden {
    display: none;
}

    </style >
</head>
<body>
    <div class="container">
        <h2>Login</h2>
        <form id="login-form">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>
        <button id="logout-button" class="hidden">Logout</button>
    </div>
    
    <script src="script.js">
    const loginForm = document.getElementById('login-form');
const logoutButton = document.getElementById('logout-button');

loginForm.addEventListener('submit', function (event) {
    event.preventDefault();

    // Simulate a login by checking the credentials (replace with your logic)
    const username = document.getElementById('username').value;
    const password = document.getElementById('password').value;

    if (username === 'user' && password === 'password') {
        // Successful login
        loginForm.reset(); // Clear input fields
        loginForm.classList.add('hidden'); // Hide login form
        logoutButton.classList.remove('hidden'); // Show logout button
    } else {
        alert('Invalid username or password');
    }
});

logoutButton.addEventListener('click', function () {
    loginForm.classList.remove('hidden'); // Show login form
    logoutButton.classList.add('hidden'); // Hide logout button
});

    </script>
</body>
</html>
