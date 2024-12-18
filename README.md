<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Form Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #5F9EA0;
        }
        .login-container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .login-container h2 {
            margin-bottom: 20px;
            text-align: center;
        }
        .login-container label {
            display: block;
            margin-bottom: 5px;
        }
        .login-container input {
            width: 100%;
            padding: 5px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .login-container button {
            width: 100%;
            padding: 10px;
            background: #5F9EA0;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .login-container button:hover {
            background:#008080;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <form id="loginForm">
            <label for="username">Username</label>
            <input type="text" id="username" name="username" required>

            <label for="password">Password</label>
            <input type="password" id="password" name="password" required>

            <button type="submit">Login</button>
        </form>
    </div>

    <script>
        document.getElementById('loginForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Mencegah form submit secara default

            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            // Simpan data ke Local Storage
            localStorage.setItem('username', username);
            localStorage.setItem('password', password);

            alert('Data berhasil disimpan!');

            // Arahkan ke halaman lain setelah login (opsional)
            window.location.href = 'spldv.html';
        });
    </script>
</body>
</html>
