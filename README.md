# mhanki-gold.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday! 🎂🐱</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:'Trebuchet MS',sans-serif;
}

body{
    overflow:hidden;
    background:linear-gradient(135deg,#ffd6e8,#ffe9c9,#d9f7ff);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    position:relative;
}

/* Floating Balloons */
.balloon{
    position:absolute;
    bottom:-180px;
    width:70px;
    height:90px;
    border-radius:50%;
    animation:float linear infinite;
}

.balloon::after{
    content:'';
    position:absolute;
    width:2px;
    height:80px;
    background:#888;
    left:50%;
    top:90px;
}

@keyframes float{
    from{
        transform:translateY(0);
    }
    to{
        transform:translateY(-130vh);
    }
}

.container{
    width:90%;
    max-width:750px;
    background:rgba(255,255,255,.85);
    backdrop-filter:blur(8px);
    border-radius:30px;
    padding:40px;
    text-align:center;
    box-shadow:0 20px 50px rgba(0,0,0,.15);
    z-index:10;
}

h1{
    color:#ff5d94;
    font-size:2.8rem;
}

.subtitle{
    color:#666;
    margin:15px 0 25px;
    font-size:1.1rem;
}

/* Cute Cat */
.cat{
    font-size:110px;
    animation:bounce 2s infinite;
}

@keyframes bounce{
    0%,100%{
        transform:translateY(0);
    }
    50%{
        transform:translateY(-12px);
    }
}

button{
    margin-top:25px;
    padding:15px 35px;
    border:none;
    border-radius:50px;
    background:#ff7db7;
    color:white;
    font-size:1.1rem;
    cursor:pointer;
    transition:.3s;
    box-shadow:0 8px 18px rgba(255,125,183,.4);
}

button:hover{
    transform:scale(1.08);
    background:#ff4f9a;
}

.message{
    margin-top:30px;
    display:none;
    animation:fadeIn 1s;
}

.message h2{
    color:#ff5d94;
    margin-bottom:15px;
}

.message p{
    font-size:1.1rem;
    line-height:1.8;
    color:#444;
}

@keyframes fadeIn{
    from{
        opacity:0;
        transform:translateY(20px);
    }
    to{
        opacity:1;
        transform:translateY(0);
    }
}

.hearts{
    font-size:30px;
    margin-top:20px;
    animation:pulse 1s infinite;
}

@keyframes pulse{
    50%{
        transform:scale(1.2);
    }
}

.sparkle{
    position:absolute;
    font-size:22px;
    animation:twinkle 3s infinite;
}

@keyframes twinkle{
    0%,100%{
        opacity:.3;
        transform:scale(.7);
    }
    50%{
        opacity:1;
        transform:scale(1.3);
    }
}
</style>
</head>

<body>

<!-- Balloons -->
<div class="balloon" style="left:5%;background:#ff8fa3;animation-duration:12s;"></div>
<div class="balloon" style="left:15%;background:#ffd166;animation-duration:10s;"></div>
<div class="balloon" style="left:28%;background:#90dbf4;animation-duration:14s;"></div>
<div class="balloon" style="left:42%;background:#caffbf;animation-duration:13s;"></div>
<div class="balloon" style="left:58%;background:#ffafcc;animation-duration:11s;"></div>
<div class="balloon" style="left:72%;background:#bdb2ff;animation-duration:15s;"></div>
<div class="balloon" style="left:85%;background:#f7b267;animation-duration:12s;"></div>
<div class="balloon" style="left:95%;background:#a0c4ff;animation-duration:10s;"></div>

<!-- Sparkles -->
<div class="sparkle" style="left:8%;top:15%;">✨</div>
<div class="sparkle" style="left:20%;top:8%;">⭐</div>
<div class="sparkle" style="left:80%;top:12%;">✨</div>
<div class="sparkle" style="left:90%;top:22%;">🌟</div>
<div class="sparkle" style="left:70%;top:80%;">✨</div>
<div class="sparkle" style="left:12%;top:75%;">⭐</div>

<div class="container">

    <div class="cat">🐱🎀</div>

    <h1>Happy Birthday!</h1>

    <p class="subtitle">
        Wishing you the happiest and cutest birthday ever! 🎂
    </p>

    <button onclick="showMessage()">
        🎁 Open Your Birthday Surprise
    </button>

    <div class="message" id="message">

        <h2>🎉 Surprise! 🎉</h2>

        <p>
            Happy Birthday to babu dolly my mama! legal kana pede na tayo kasal 💖<br><br>

            May your special day be filled with endless smiles,
            warm hugs, sweet surprises, and beautiful memories.
            Just like this little kitty, may your life always be
            surrounded by love, happiness, good health, and lots of laughter.
            <br><br>

            Keep believing in your dreams, keep shining brightly,
            and never stop being the amazing person you are.
            You deserve every happiness today and always.
            <br><br>

            🎂 Have an unforgettable birthday! -mhanki 🎈🎁✨
        </p>

        <div class="hearts">
            💖 🐱 🎉 🎂 🎈 🌸 💕
        </div>

    </div>

</div>

<script>
function showMessage(){

    document.getElementById("message").style.display="block";

    // Confetti
    for(let i=0;i<120;i++){

        const confetti=document.createElement("div");

        confetti.innerHTML=["🎉","🎊","✨","💖","🎈","🌸","⭐"][Math.floor(Math.random()*7)];

        confetti.style.position="fixed";
        confetti.style.left=Math.random()*100+"vw";
        confetti.style.top="-20px";
        confetti.style.fontSize=(18+Math.random()*18)+"px";
        confetti.style.transition="transform 4s linear, opacity 4s";
        confetti.style.pointerEvents="none";

        document.body.appendChild(confetti);

        setTimeout(()=>{
            confetti.style.transform=`translateY(${window.innerHeight+100}px) rotate(${Math.random()*720}deg)`;
            confetti.style.opacity=0;
        },50);

        setTimeout(()=>{
            confetti.remove();
        },4200);
    }
}
</script>

</body>
</html>
