<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Just Asking 😊</title>

<style>
    body {
        background: linear-gradient(135deg, #fbc2eb, #a6c1ee);
        font-family: Arial, sans-serif;
        height: 100vh;
        margin: 0;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .card {
        background: white;
        width: 85%;
        max-width: 360px;
        padding: 30px 22px;
        border-radius: 22px;
        text-align: center;
        box-shadow: 0 20px 40px rgba(0,0,0,0.25);
        position: relative;
        z-index: 10;
    }

    h1 {
        color: #6a5acd;
        font-size: 22px;
        line-height: 1.4;
        margin-bottom: 12px;
    }

    p {
        color: #555;
        font-size: 14px;
        margin-bottom: 25px;
    }

    .buttons {
        position: relative;
        height: 130px;
    }

    button {
        padding: 14px 26px;
        font-size: 18px;
        border-radius: 30px;
        border: none;
        cursor: pointer;
        transition: all 0.25s ease;
    }

    #yes {
        background-color: #6a5acd;
        color: white;
    }

    #no {
        background-color: #eee;
        color: #999;
        position: absolute;
        left: 50%;
        top: 65px;
        transform: translateX(-50%);
    }
</style>
</head>

<body>

<div class="card">
    <h1>Hey Smriti 🌸</h1>

    <h1>Can we meet now?</h1>

    <p>(now I have learned coding also for you)</p>

    <div class="buttons">
        <button id="yes" onclick="yesClicked()">YES 😊</button>
        <button id="no">NO 🙈</button>
    </div>
</div>

<script>
    const noBtn = document.getElementById("no");

    function moveNo() {
        const x = Math.random() * (window.innerWidth - 120);
        const y = Math.random() * (window.innerHeight - 120);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    }

    // Mobile touch
    noBtn.addEventListener("touchstart", moveNo);
    // Desktop fallback
    noBtn.addEventListener("mouseover", moveNo);

    function yesClicked() {
        document.body.innerHTML = `
        <div style="
            height:100vh;
            display:flex;
            justify-content:center;
            align-items:center;
            text-align:center;
            background:linear-gradient(135deg,#cfd9df,#e2ebf0);
            font-family:Arial;
            padding:20px;
        ">
            <h1 style="color:#6a5acd; line-height:1.5;">
                Yay 😄<br><br>
                That was worth learning coding for 💻✨<br><br>
                See you soon 🌸
            </h1>
        </div>
        `;
    }
</script>

</body>
</html>
