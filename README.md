<!DOCTYPE html>
<html>
<head>
    <title>For Garima ❤️</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            text-align: center;
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
        }

        h1 {
            margin-top: 100px;
            font-size: 42px;
            color: white;
        }

        p {
            max-width: 600px;
            margin: 20px auto;
            font-size: 20px;
            color: white;
            line-height: 1.6;
        }

        .btn {
            padding: 15px 30px;
            font-size: 22px;
            border: none;
            border-radius: 12px;
            cursor: pointer;
            position: absolute;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
            left: 45%;
            top: 65%;
        }

        #noBtn {
            background-color: #333;
            color: white;
            left: 58%;
            top: 65%;
        }

        .heart {
            position: fixed;
            color: red;
            font-size: 20px;
            animation: floatUp 5s linear infinite;
        }

        @keyframes floatUp {
            from { transform: translateY(100vh); opacity: 1; }
            to { transform: translateY(-10vh); opacity: 0; }
        }
    </style>
</head>
<body>

<h1>Garima, will you be my Valentine? 💖</h1>

<p>
From the moment you came into my life, everything feels brighter and happier.  
Your smile, your kindness, and the way you make even normal days special means more to me than you know.  
I’m really lucky to have you, and I’d love to make more memories together.  
So… will you be my Valentine? ❤️
</p>

<button id="yesBtn" class="btn" onclick="yesClicked()">Yes ❤️</button>
<button id="noBtn" class="btn">No 😈</button>

<script>
    const noBtn = document.getElementById("noBtn");

    noBtn.addEventListener("mouseover", () => {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    function yesClicked() {
        document.body.innerHTML = `
            <h1>Yay Garima said YES!! 💖🥰</h1>
            <p>This just made me the happiest person alive ❤️</p>
        `;
        document.body.style.background = "#ff4d6d";
    }

    // Floating hearts
    setInterval(() => {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerHTML = "❤️";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.fontSize = (Math.random() * 20 + 15) + "px";
        document.body.appendChild(heart);

        setTimeout(() => {
            heart.remove();
        }, 5000);
    }, 300);
</script>

</body>
</html>
