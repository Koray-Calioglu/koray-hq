<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KORAY HQ | Uzay Uygulaması</title>
    <style>
        body {
            background-color: #050505;
            color: #00ffcc;
            font-family: 'Courier New', Courier, monospace;
            margin: 0;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        /* Arka plandaki yıldız efekti */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(2px 2px at 20px 30px, #eee, rgba(0,0,0,0)),
                        radial-gradient(2px 2px at 40px 70px, #fff, rgba(0,0,0,0)),
                        radial-gradient(2px 2px at 50px 160px, #ddd, rgba(0,0,0,0));
            background-repeat: repeat;
            background-size: 200px 200px;
            animation: zoom 10s infinite linear;
            z-index: -1;
        }

        @keyframes zoom {
            from { transform: scale(1); }
            to { transform: scale(1.5); }
        }

        .terminal {
            width: 80%;
            max-width: 800px;
            background: rgba(0, 20, 20, 0.9);
            border: 1px solid #00ffcc;
            box-shadow: 0 0 20px #00ffcc;
            padding: 20px;
            border-radius: 10px;
            position: relative;
        }

        .terminal-header {
            border-bottom: 1px solid #00ffcc;
            padding-bottom: 10px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            font-weight: bold;
        }

        .ai-status {
            animation: blink 1s infinite;
        }

        @keyframes blink {
            50% { opacity: 0; }
        }

        .command-line {
            margin: 10px 0;
            font-size: 1.1rem;
        }

        .typing {
            overflow: hidden;
            white-space: nowrap;
            border-right: .15em solid #00ffcc;
            animation: typing 3.5s steps(40, end), blink-caret .75s step-end infinite;
        }

        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #00ffcc; }
        }

        .footer-info {
            margin-top: 30px;
            font-size: 0.8rem;
            opacity: 0.6;
        }

        .scanner {
            width: 100%;
            height: 2px;
            background: #00ffcc;
            position: absolute;
            top: 0;
            left: 0;
            animation: scan 4s infinite linear;
            opacity: 0.3;
        }

        @keyframes scan {
            0% { top: 0; }
            100% { top: 100%; }
        }
    </style>
</head>
<body>

    <div class="stars"></div>

    <div class="terminal">
        <div class="scanner"></div>
        <div class="terminal-header">
            <span>KORAY_OS_V1.0</span>
            <span class="ai-status">● AI LINK ACTIVE</span>
        </div>

        <div class="command-line">>> İSİM: KORAY</div>
        <div class="command-line">>> LOKASYON: DÜNYA SEKTÖRÜ</div>
        <div class="command-line">>> GÖREV: EVRENİN SINIRLARINI KEŞFETMEK</div>
        <hr style="border: 0.5px solid #00ffcc; margin: 20px 0;">
        
        <div class="command-line typing" style="color: #ffcc00;">[SİSTEM]: Gemini AI protokolü bağlandı...</div>
        <div class="command-line" style="margin-top: 15px;">>> Veriler analiz ediliyor...</div>
        <div class="command-line">>> Uzay Uygulaması başarıyla başlatıldı.</div>
        
        <div class="footer-info">
            * Gizli API Anahtarı arka planda otomatik olarak kullanılır.
        </div>
    </div>

    <p style="margin-top: 20px; font-size: 0.9rem;">Sistem yarınki ders için hazır.</p>

</body>
</html>
        
