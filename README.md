<div style="text-align: center; margin-top: 50px;">
    <button onclick="ureyYagdir()" id="heartBtn">❤️ Qırmızı ürəyə bas</button>
</div>

<style>
    #heartBtn {
        padding: 20px 40px;
        font-size: 24px;
        background-color: #ff4d4d;
        color: white;
        border: none;
        border-radius: 50px;
        cursor: pointer;
        font-weight: bold;
        box-shadow: 0 5px 15px rgba(255, 77, 77, 0.4);
        transition: transform 0.2s;
    }

    #heartBtn:hover {
        transform: scale(1.1);
        background-color: #ff1a1a;
    }

    .falling-heart {
        position: fixed;
        top: -20px;
        font-size: 20px;
        user-select: none;
        pointer-events: none;
        z-index: 9999;
        animation: fall linear forwards;
    }

    @keyframes fall {
        to {
            transform: translateY(100vh) rotate(360deg);
            opacity: 0;
        }
    }
</style>

<script>
    function ureyYagdir() {
        // Tam 1000 ədəd (və ya istədiyin qədər) ürək üçün
        for (let i = 0; i < 200; i++) { 
            setTimeout(() => {
                const heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.classList.add('falling-heart');
                
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.animationDuration = (Math.random() * 2 + 2) + 's';
                heart.style.fontSize = (Math.random() * 20 + 15) + 'px';
                
                document.body.appendChild(heart);
                
                setTimeout(() => {
                    heart.remove();
                }, 4000);
            }, i * 20); // Ürəklərin sürətlə ard-arda çıxması üçün
        }
    }
</script>
