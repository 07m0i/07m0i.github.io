# 07m0i.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Security Awareness Demo</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Courier New', monospace;
            background-color: #0a0a1a;
            background-image: 
                radial-gradient(circle at 75% 30%, rgba(0, 100, 255, 0.1) 0%, transparent 25%),
                radial-gradient(circle at 25% 70%, rgba(255, 50, 150, 0.1) 0%, transparent 25%);
            color: #e0e0e0;
            overflow-x: hidden;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            border-bottom: 1px solid #333;
            padding-bottom: 20px;
            position: relative;
        }

        h1 {
            color: #ff3366;
            text-shadow: 0 0 10px rgba(255, 51, 102, 0.5);
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #33ccff;
            font-size: 1.2rem;
            margin-top: 0;
        }

        .content {
            background-color: rgba(20, 20, 40, 0.8);
            border-radius: 5px;
            padding: 30px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            position: relative;
            z-index: 1;
        }

        .hacker-text {
            font-family: 'Courier New', monospace;
            white-space: pre;
            line-height: 1.4;
            color: #33ff33;
        }

        .signature {
            text-align: right;
            margin-top: 40px;
            font-style: italic;
            color: #ff9933;
        }

        .team-badge {
            position: absolute;
            top: 20px;
            right: 20px;
            background: linear-gradient(45deg, #ff3366, #9933ff);
            padding: 10px 15px;
            border-radius: 5px;
            transform: rotate(5deg);
            box-shadow: 0 0 15px rgba(153, 51, 255, 0.5);
            font-weight: bold;
        }

        .glowing-text {
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px #33ccff, 0 0 20px #33ccff;
            }
            to {
                text-shadow: 0 0 10px #fff, 0 0 15px #ff66b2, 0 0 20px #ff66b2, 0 0 25px #ff66b2;
            }
        }

        .binary-rain {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 0;
            opacity: 0.15;
            pointer-events: none;
        }

        .warning {
            background-color: rgba(255, 50, 50, 0.2);
            border-left: 3px solid #ff3366;
            padding: 15px;
            margin: 20px 0;
            border-radius: 0 5px 5px 0;
        }
    </style>
</head>
<body>
    <div class="binary-rain" id="binaryRain"></div>
    
    <div class="container">
        <div class="team-badge glowing-text">TEAM 104</div>
        
        <div class="header">
            <h1>TEAM 104</h1>
            <p class="subtitle">07m0i IS EVERYWHERE!</p>
        </div>
        
        <div class="content">
            <div class="warning">
                <strong>INFORMATION:</strong> We Hacked the official website of the iraqi forces
            </div>
            
            <div class="hacker-text">
[!] Security: Vulnerability Detected
[!] Target: iraqs military
[!] Method: SLQ INJECTION
[!] Status: <span style="color:#ff3366">VULNERABLE</span>

[+] Bypassing Authentication... <span style="color:#33ff33">SUCCESS</span>
[+] Accessing Restricted Endpoints... <span style="color:#33ff33">SUCCESS</span>
[+] Extracting Sample Data... <span style="color:#33ff33">COMPLETE</span>

============================================
this attack was carried on by 104!
============================================
            </div>
            
            <div class="signature">
                <p>Security Research Demonstration</p>
                <p style="color:#33ccff;font-weight:bold;">hacked by 07m0i</p>
            </div>
        </div>
    </div>

    <script>
        // Binary rain effect
        const binaryRain = document.getElementById('binaryRain');
        const characters = '01';
        const columns = Math.floor(window.innerWidth / 20);
        
        for (let i = 0; i < columns; i++) {
            const column = document.createElement('div');
            column.style.position = 'absolute';
            column.style.top = '-50px';
            column.style.left = (i * 20) + 'px';
            column.style.width = '20px';
            column.style.fontSize = '16px';
            column.style.color = i % 2 === 0 ? '#33ccff' : '#ff3366';
            column.style.opacity = Math.random() * 0.5 + 0.1;
            column.style.animation = `fall ${Math.random() * 5 + 3}s linear infinite`;
            column.style.animationDelay = `${Math.random() * 2}s`;
            
            let content = '';
            for (let j = 0; j < 30; j++) {
                content += characters.charAt(Math.floor(Math.random() * characters.length)) + '<br>';
            }
            column.innerHTML = content;
            
            binaryRain.appendChild(column);
        }
        
        // Add CSS for animation
        const style = document.createElement('style');
        style.innerHTML = `
            @keyframes fall {
                to { transform: translateY(calc(100vh + 50px)); }
            }
        `;
        document.head.appendChild(style);
    </script>
</html>
