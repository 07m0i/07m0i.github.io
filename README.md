<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>SYSTEM BREACHED</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background-color: #000;
            color: #ff0000;
            font-family: 'Courier New', monospace;
            overflow: hidden;
            touch-action: none;
            height: 100vh;
            width: 100vw;
        }

        .matrix-rain {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
            opacity: 0.15;
            pointer-events: none;
        }

        .hacked-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 100;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 10px;
        }

        .hacked-header {
            text-align: center;
            font-size: 2rem;
            text-shadow: 0 0 10px #ff0000;
            animation: glitch 1s linear infinite;
            margin-top: 10vh;
        }

        @keyframes glitch {
            0% { transform: translate(0); text-shadow: 0 0 10px #ff0000; }
            25% { transform: translate(-2px, 2px); text-shadow: 2px -2px 5px #ff0000; }
            50% { transform: translate(2px, -1px); text-shadow: -2px 2px 5px #ff0000; }
            75% { transform: translate(-1px, 1px); text-shadow: 1px -1px 5px #ff0000; }
            100% { transform: translate(0); text-shadow: 0 0 10px #ff0000; }
        }

        .hacked-subheader {
            font-size: 1.2rem;
            text-align: center;
            margin: 10px 0;
            animation: flicker 3s infinite;
        }

        @keyframes flicker {
            0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% { opacity: 1; }
            20%, 22%, 24%, 55% { opacity: 0.7; }
        }

        .console {
            background-color: rgba(0, 0, 0, 0.7);
            border: 1px solid #ff0000;
            border-radius: 5px;
            padding: 10px;
            height: 40vh;
            overflow-y: auto;
            font-size: 0.9rem;
            margin-bottom: 10px;
        }

        .console-line {
            margin: 3px 0;
            color: #ff0000;
            white-space: nowrap;
            overflow: hidden;
            animation: typing 0.1s steps(40, end);
        }

        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }

        .hex-data {
            position: absolute;
            color: rgba(255, 0, 0, 0.3);
            font-size: 0.7rem;
            font-family: monospace;
            pointer-events: none;
            z-index: 1;
            animation: float 20s linear infinite;
        }

        @keyframes float {
            0% { transform: translateY(100vh) translateX(0); opacity: 0; }
            10% { opacity: 0.3; }
            90% { opacity: 0.3; }
            100% { transform: translateY(-100px) translateX(20px); opacity: 0; }
        }

        .scanlines {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(
                to bottom,
                transparent 95%,
                rgba(255, 0, 0, 0.05) 95%
            );
            background-size: 100% 5px;
            z-index: 50;
            pointer-events: none;
            animation: scanline 8s linear infinite;
        }

        @keyframes scanline {
            0% { background-position: 0 0; }
            100% { background-position: 0 100%; }
        }

        .bitcoin-demand {
            background: rgba(0, 0, 0, 0.8);
            border: 1px solid #ff0000;
            padding: 10px;
            margin: 10px 0;
            text-align: center;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 5px rgba(255, 0, 0, 0.3); }
            50% { box-shadow: 0 0 15px rgba(255, 0, 0, 0.5); }
            100% { box-shadow: 0 0 5px rgba(255, 0, 0, 0.3); }
        }

        .ip-info {
            font-size: 0.8rem;
            text-align: center;
            margin-bottom: 10px;
        }

        .hacking-progress {
            height: 5px;
            background: rgba(255, 0, 0, 0.2);
            margin: 5px 0;
            border-radius: 5px;
            overflow: hidden;
        }

        .progress-bar {
            height: 100%;
            background: #ff0000;
            width: 0%;
            animation: progress 10s linear infinite;
        }

        @keyframes progress {
            0% { width: 0%; }
            50% { width: 100%; }
            100% { width: 0%; }
        }
    </style>
</head>
<body>
    <canvas id="matrix" class="matrix-rain"></canvas>
    <div class="scanlines"></div>
    
    <div class="hacked-overlay">
        <div>
            <div class="hacked-header">FUCKED BY D5RKSIDE</div>
            <div class="hacked-subheader">SYSTEM TAKEOVER COMPLETE</div>
            
            <div class="ip-info">
                IP: 192.168.1.105 | LOCATION: TRACKED | ISP: LOGGED
            </div>
            
            <div class="bitcoin-demand">
                YOUR FILES ARE ENCRYPTED<br>
                PAY 0.5 BTC TO:<br>
                bc1qxy2kgdygjrsqtzq2n0yrf249nw6k2g0j8s8k7r<br>
                <div class="hacking-progress">
                    <div class="progress-bar"></div>
                </div>
                TIME REMAINING: <span id="countdown">23:59:59</span>
            </div>
        </div>
        
        <div class="console" id="console">
            <div class="console-line">> Initializing D5RKSIDE payload...</div>
            <div class="console-line">> Exploiting CVE-2023-4863 (Chrome 0-day)...</div>
            <div class="console-line">> Bypassing ASLR... SUCCESS</div>
            <div class="console-line">> Escalating to root... SUCCESS</div>
            <div class="console-line">> Installing persistent backdoor...</div>
            <div class="console-line">> Backdoor active at /usr/bin/.libsystemd</div>
            <div class="console-line">> Dumping browser credentials...</div>
            <div class="console-line">> Extracting 12,456 login pairs</div>
            <div class="console-line">> Encrypting files with RSA-4096...</div>
            <div class="console-line">> Establishing TOR connection...</div>
            <div class="console-line">> Exfiltrating data to onion service...</div>
        </div>
    </div>

    <script>
        // Matrix rain background
        const canvas = document.getElementById('matrix');
        const ctx = canvas.getContext('2d');
        
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
        
        const katakana = 'アァカサタナハマヤャラワガザダバパイィキシチニヒミリヰギジヂビピウゥクスツヌフムユュルグズブヅプエェケセテネヘメレヱゲゼデベペオォコソトノホモヨョロヲゴゾドボポヴッン';
        const latin = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
        const nums = '0123456789';
        const hex = '0123456789ABCDEF';
        
        const alphabet = katakana + latin + nums + hex;
        
        const fontSize = 14;
        const columns = canvas.width / fontSize;
        
        const rainDrops = [];
        
        for (let x = 0; x < columns; x++) {
            rainDrops[x] = 1;
        }
        
        const draw = () => {
            ctx.fillStyle = 'rgba(0, 0, 0, 0.05)';
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            ctx.fillStyle = '#ff0000';
            ctx.font = fontSize + 'px monospace';
            
            for (let i = 0; i < rainDrops.length; i++) {
                const text = alphabet.charAt(Math.floor(Math.random() * alphabet.length));
                ctx.fillText(text, i * fontSize, rainDrops[i] * fontSize);
                
                if (rainDrops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                    rainDrops[i] = 0;
                }
                rainDrops[i]++;
            }
        };
        
        setInterval(draw, 30);

        // Create floating hex data
        function createHexData() {
            const hexData = document.createElement('div');
            hexData.className = 'hex-data';
            
            let hexString = '';
            for (let i = 0; i < 40; i++) {
                hexString += Math.floor(Math.random() * 16).toString(16).toUpperCase();
                if (i % 4 === 3) hexString += ' ';
            }
            
            hexData.textContent = hexString;
            hexData.style.left = Math.random() * 100 + 'vw';
            hexData.style.animationDuration = (10 + Math.random() * 20) + 's';
            hexData.style.animationDelay = Math.random() * 5 + 's';
            
            document.body.appendChild(hexData);
            
            setTimeout(() => {
                hexData.remove();
            }, 30000);
        }
        
        setInterval(createHexData, 500);

        // Console output
        const consoleEl = document.getElementById('console');
        const hackMessages = [
            "> Injecting meterpreter shell...",
            "> Migrating to explorer.exe...",
            "> Dumping LSASS memory...",
            "> Harvesting browser cookies...",
            "> Found 23 saved credit cards",
            "> Accessing webcam feed...",
            "> Recording microphone input...",
            "> Scanning local network...",
            "> Brute-forcing router admin...",
            "> Router compromised: 192.168.1.1",
            "> Disabling firewall...",
            "> Modifying system logs...",
            "> Creating admin user: D5RKSIDE_ADMIN",
            "> Installing keylogger...",
            "> Keylogger active on all inputs",
            "> Capturing screenshots every 30s",
            "> BTC transaction received: 0.025 BTC",
            "> Total BTC: 1.245",
            "> New victim infected: 192.168.1.107",
            "> Lateral movement successful",
            "> Deploying ransomware to 3 new hosts"
        ];
        
        let messageIndex = 0;
        const consoleInterval = setInterval(() => {
            if (messageIndex >= hackMessages.length) {
                messageIndex = 0;
            }
            
            const line = document.createElement('div');
            line.className = 'console-line';
            line.textContent = hackMessages[messageIndex];
            consoleEl.appendChild(line);
            consoleEl.scrollTop = consoleEl.scrollHeight;
            messageIndex++;
        }, 1500);

        // Countdown timer
        const countdownEl = document.getElementById('countdown');
        let totalSeconds = 86399; // 23:59:59
        
        const countdownInterval = setInterval(() => {
            totalSeconds--;
            
            const hours = Math.floor(totalSeconds / 3600);
            const minutes = Math.floor((totalSeconds % 3600) / 60);
            const seconds = totalSeconds % 60;
            
            countdownEl.textContent = 
                `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')}`;
            
            if (totalSeconds <= 0) {
                clearInterval(countdownInterval);
            }
        }, 1000);

        // Window resize handler
        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });
    </script>
</body>
</html>
