height && Math.random() > 0.975) {
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
                ${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}:${seconds.toString().padStart(2, '0')};
            
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
