<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TIKTOK FUCKER v1.0 | 07M0i</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&display=swap');
        
        :root {
            --hacker-green: #00ff41;
            --matrix-dark: #0d0208;
            --glow: 0 0 10px var(--hacker-green);
        }
        
        body {
            margin: 0;
            padding: 0;
            background: var(--matrix-dark);
            color: var(--hacker-green);
            font-family: 'JetBrains Mono', monospace;
            overflow-x: hidden;
            line-height: 1.6;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem;
            border: 1px solid var(--hacker-green);
            box-shadow: var(--glow);
            background: rgba(13, 2, 8, 0.8);
        }
        
        h1 {
            text-align: center;
            text-shadow: var(--glow);
            margin-bottom: 2rem;
            font-weight: 700;
            letter-spacing: -1px;
        }
        
        .tagline {
            text-align: center;
            margin-bottom: 3rem;
            border-bottom: 1px dashed var(--hacker-green);
            padding-bottom: 1rem;
        }
        
        .input-box {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
        }
        
        input {
            background: transparent;
            border: 1px solid var(--hacker-green);
            color: var(--hacker-green);
            padding: 0.8rem 1.5rem;
            font-family: 'JetBrains Mono', monospace;
            width: 70%;
            outline: none;
            box-shadow: var(--glow);
        }
        
        input::placeholder {
            color: rgba(0, 255, 65, 0.5);
        }
        
        button {
            background: transparent;
            border: 1px solid var(--hacker-green);
            color: var(--hacker-green);
            padding: 0.8rem 2rem;
            font-family: 'JetBrains Mono', monospace;
            cursor: pointer;
            margin-left: 0.5rem;
            box-shadow: var(--glow);
            transition: all 0.3s;
        }
        
        button:hover {
            background: rgba(0, 255, 65, 0.1);
        }
        
        .results {
            border: 1px solid var(--hacker-green);
            padding: 1.5rem;
            margin-top: 2rem;
            box-shadow: var(--glow);
            display: none;
        }
        
        .result-line {
            margin: 0.5rem 0;
            font-size: 0.9rem;
        }
        
        .signature {
            text-align: right;
            margin-top: 3rem;
            font-style: italic;
            opacity: 0.7;
        }
        
        .blink {
            animation: blink 1s infinite;
        }
        
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
        
        /* Terminal-like typing effect */
        .typing {
            border-right: 2px solid var(--hacker-green);
            animation: typing 0.5s step-end infinite alternate;
        }
        
        @keyframes typing {
            from { border-color: transparent; }
            to { border-color: var(--hacker-green); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>TIKTOK FUCKER v1.0</h1>
        <div class="tagline">
            [ EXTRACTING FOLLOWING LISTS SINCE 2024 | PRIVATE ACCOUNTS? NO PROBLEM ]
        </div>
        
        <div class="input-box">
            <input type="text" id="username" placeholder="@username" class="typing">
            <button id="analyze-btn">EXECUTE</button>
        </div>
        
        <div class="results" id="results">
            <div class="result-line">> INITIALIZING TIKTOK API BYPASS...</div>
            <div class="result-line">> SCRAPING FOLLOWING DATA...</div>
            <div class="result-line">> ANALYZING ENGAGEMENT PATTERNS...</div>
            <div class="result-line">> FOUND <span id="count">0</span> FOLLOWING ACCOUNTS</div>
            <div class="result-line">> PRIVATE STATUS: <span id="private-status">UNKNOWN</span></div>
            <div class="result-line">> MOST ACTIVE TIME: <span id="active-time">--:--</span></div>
            <div class="result-line">> VERIFIED ACCOUNTS: <span id="verified-count">0</span></div>
            <div class="result-line">> FULL LIST EXPORTED TO: <span id="export-path">./data/<span id="filename">user_data.txt</span></span></div>
            <div class="result-line">> <span class="blink">READY FOR NEXT TARGET</span></div>
        </div>
        
        <div class="signature">
            FUCKED BY 07M0i
        </div>
    </div>
    
    <script>
        document.getElementById('analyze-btn').addEventListener('click', function() {
            const username = document.getElementById('username').value.trim();
            
            if (!username) {
                alert('> ERROR: NO USERNAME PROVIDED');
                return;
            }
            
            this.textContent = 'SCANNING...';
            this.disabled = true;
            
            // Simulate hacking effect
            const resultLines = document.querySelectorAll('.result-line');
            resultLines.forEach((line, index) => {
                setTimeout(() => {
                    line.style.opacity = '1';
                }, index * 300);
            });
            
            setTimeout(() => {
                document.getElementById('results').style.display = 'block';
                document.getElementById('count').textContent = Math.floor(Math.random() * 500) + 100;
                document.getElementById('private-status').textContent = Math.random() > 0.5 ? 'BREACHED' : 'PUBLIC';
                document.getElementById('active-time').textContent = `${Math.floor(Math.random() * 12) + 1}:${Math.floor(Math.random() * 60).toString().padStart(2, '0')} PM`;
                document.getElementById('verified-count').textContent = Math.floor(Math.random() * 20);
                document.getElementById('filename').textContent = `${username}_data.txt`;
                
                this.textContent = 'EXECUTE';
                this.disabled = false;
            }, 2500);
        });
    </script>
</body>
</html>
