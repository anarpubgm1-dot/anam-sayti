<!DOCTYPE html>
<html lang="az">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Anama Sürpriz ❤️</title>
    <style>
        body {
            margin: 0; padding: 0; display: flex; flex-direction: column;
            align-items: center; justify-content: center; min-height: 100vh;
            background-color: #fff5f7; font-family: sans-serif; text-align: center;
            overflow: hidden;
        }
        .sheir {
            background: white; padding: 20px; border-radius: 15px;
            margin-bottom: 20px; box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        h1 { color: #d63384; margin: 10px 0; }
        #ureyBtn {
            padding: 15px 30px; font-size: 20px; background: #ff4d4d;
            color: white; border: none; border-radius: 50px; cursor: pointer;
            box-shadow: 0 5px 15px rgba(255, 77, 77, 0.4);
        }
        .falling-heart {
            position: fixed; top: -20px; z-index: 999;
            pointer-events: none; animation: fall linear forwards;
        }
        @keyframes fall {
            to { transform: translateY(105vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="sheir">
        <p>Günəş tək nur saçar hər bir sözünlə,</p>
        <p>Dünyanı bəzərsən gülər üzünlə.</p>
        <p>Sən mənim dünyamsan, əziz canımsan,</p>
        <p>Yaxşı ki, varsan, mənim Anamsan!</p>
    </div>

    <h1>Canım Anam ❤️</h1>
    <button id="ureyBtn">Qırmızı ürəyə bas</button>

    <script>
        document.getElementById('ureyBtn').addEventListener('click', function() {
            for (let i = 0; i < 200; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.innerHTML = '❤️';
                    heart.className = 'falling-heart';
                    heart.style.left = Math.random() * 100 + 'vw';
                    heart.style.animationDuration = (Math.random() * 2 + 2) + 's';
                    heart.style.fontSize = (Math.random() * 20 + 10) + 'px';
                    document.body.appendChild(heart);
                    setTimeout(() => { heart.remove(); }, 4000);
                }, i * 20);
            }
        });
    </script>
</body>
</html>
