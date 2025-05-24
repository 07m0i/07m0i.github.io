<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TikTok Following Analyzer | 07M0i</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');
        
        :root {
            --primary: #25F4EE;
            --secondary: #FE2C55;
            --dark: #010101;
            --light: #FFFFFF;
            --gray: #F1F1F2;
        }
        
        body {
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, var(--dark), #1A1A1D);
            color: var(--light);
            min-height: 100vh;
            overflow-x: hidden;
            background-image: 
                radial-gradient(circle at 25% 25%, rgba(37, 244, 238, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 75% 75%, rgba(254, 44, 85, 0.1) 0%, transparent 50%);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        
        .creator-text {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
            text-shadow: 0 0 10px rgba(37, 244, 238, 0.3);
            animation: glow 2s infinite alternate;
        }
        
        @keyframes glow {
            from {
                text-shadow: 0 0 10px rgba(37, 244, 238, 0.3);
            }
            to {
                text-shadow: 0 0 20px rgba(37, 244, 238, 0.6), 0 0 30px rgba(254, 44, 85, 0.4);
            }
        }
        
        .analyzer-box {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 3rem;
            width: 100%;
            max-width: 600px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }
        
        .analyzer-box::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                to bottom right,
                transparent 0%,
                transparent 45%,
                rgba(37, 244, 238, 0.1) 50%,
                transparent 55%,
                transparent 100%
            );
            animation: rotate 20s linear infinite;
            z-index: -1;
        }
        
        @keyframes rotate {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }
        
        .username-box {
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid rgba(255, 255, 255, 0.2);
            border-radius: 12px;
            padding: 1.5rem;
            margin: 2rem 0;
            transition: all 0.3s ease;
        }
        
        .username-box:hover {
            border-color: var(--primary);
            box-shadow: 0 0 15px rgba(37, 244, 238, 0.3);
        }
        
        .username-input {
            background: transparent;
            border: none;
            width: 100%;
            color: var(--light);
            font-size: 1.2rem;
            text-align: center;
            outline: none;
            padding: 0.5rem;
        }
        
        .username-input::placeholder {
            color: rgba(255, 255, 255, 0.5);
        }
        
        .analyze-btn {
            background: linear-gradient(to right, var(--primary), var(--secondary));
            border: none;
            color: var(--light);
            padding: 1rem 2rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 1rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .analyze-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }
        
        .analyze-btn:active {
            transform: translateY(1px);
        }
        
        .results {
            margin-top: 2rem;
            text-align: left;
            width: 100%;
            display: none;
        }
        
        .result-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 1.5rem;
            margin-bottom: 1rem;
            border-left: 4px solid var(--primary);
        }
        
        .floating-icons {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .floating-icon {
            position: absolute;
            opacity: 0.1;
            animation: float 15s infinite linear;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
            }
        }
        
        @media (max-width: 768px
