<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Social Links</title>
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Poppins", sans-serif;
    }

    body, html {
        height: 105%;
    }

    body {
        background: #ffffff;
        display: flex;
        flex-direction: column;
        justify-content: space-between; /* প্রোফাইল উপরের দিকে, ফুটিার নিচে */
        align-items: center;
        padding: 10px 0;
        text-align: center;
    }

    /* প্রোফাইল বাটন */
    .profile {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .profile button {
        width: 145px;
        height: 145px;
        border-radius: 50%;
        border: 4px solid #00000020;
        background-image: url('https://i.postimg.cc/PqptpZdZ/7149746126664631302-avatar-png.png');
        background-size: cover;
        background-position: center;
        box-shadow: 0 0 20px rgba(0,0,0,0.15);
        cursor: pointer;
        transition: all 0.3s ease;
        outline: none;
    }

    .profile button:hover {
        transform: scale(1.08);
        box-shadow: 0 0 30px rgba(0,0,0,0.25);
    }

    /* নামের ফ্রেম */
    .name-frame {
        display: inline-block; 
        padding: 20px 40px; 
        border-radius: 25px; 
        background: #111; 
        box-shadow: 0 0 20px rgba(0,0,0,0.5), 0 0 40px rgba(0,0,0,0.3) inset;
        margin-top: 12px;
    }

    .name-frame h1 {
        font-size: 28px;
        font-weight: 700;
        background: linear-gradient(270deg, pink, orange, skyblue, red, green, yellow);
        background-size: 1200% 1200%;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        animation: gradientAnimation 8s ease infinite, glow 2s ease-in-out infinite alternate;
        text-shadow: 0 0 5px rgba(255,255,255,0.5);
        margin: 0;
    }

    @keyframes gradientAnimation {
        0% { background-position: 0% 50%; }
        50% { background-position: 100% 50%; }
        100% { background-position: 0% 50%; }
    }

    @keyframes glow {
        0% { text-shadow: 0 0 5px rgba(255,255,255,0.3), 0 0 10px rgba(255,255,255,0.2); }
        50% { text-shadow: 0 0 15px rgba(255,255,255,0.5), 0 0 25px rgba(255,255,255,0.4); }
        100% { text-shadow: 0 0 5px rgba(255,255,255,0.3), 0 0 10px rgba(255,255,255,0.2); }
    }

    /* বাটন গ্রিড */
    .buttons {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
        width: 90%;
        max-width: 400px;
        justify-items: center;
    }

    .buttons button {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        border: none;
        background: #000;
        color: #fff;
        font-size: 16px;
        font-weight: 500;
        cursor: pointer;
        box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        transition: all 0.3s ease;
    }

    .buttons button:hover {
        transform: scale(1.1);
        box-shadow: 0 8px 20px rgba(0,0,0,0.3);
    }

    /* Footer */
    footer {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 80px;
        padding: 10px 20px;
        background: #111;
        border-radius: 15px;
        box-shadow: 0 0 20px rgba(0,0,0,0.5), 0 0 40px rgba(0,0,0,0.3) inset;
    }

    footer p {
        font-size: 16px;
        font-weight: 600;
        color: #fff;
        background: linear-gradient(270deg, pink, orange, skyblue, red, green, yellow);
        background-size: 1200% 1200%;
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        animation: gradientFooter 8s ease infinite, glowFooter 2s ease-in-out infinite alternate;
        text-shadow: 0 0 5px rgba(255,255,255,0.5);
        margin: 0;
    }

    @keyframes gradientFooter {
        0% { background-position: 0% 50%; }
        50% { background-position: 100% 50%; }
        100% { background-position: 0% 50%; }
    }

    @keyframes glowFooter {
        0% { text-shadow: 0 0 5px rgba(255,255,255,0.3), 0 0 10px rgba(255,255,255,0.2); }
        50% { text-shadow: 0 0 15px rgba(255,255,255,0.5), 0 0 25px rgba(255,255,255,0.4); }
        100% { text-shadow: 0 0 5px rgba(255,255,255,0.3), 0 0 10px rgba(255,255,255,0.2); }
    }

</style>
</head>
<body>

    <div class="profile">
        <button id="profileBtn"></button>
        <div class="name-frame">
            <h1>𝐊ᴀ𝐰sᴀʀ</h1>
        </div>
    </div>

    <div class="buttons">
        <button>Facebook</button>
        <button>Instagram</button>
        <button>YouTube</button>
        <button>LinkedIn</button>
        <button>Twitter (X)</button>
        <button>Telegram</button>
        <button>WhatsApp</button>
        <button>Snapchat</button>
        <button>TikTok</button>
        <button>Website</button>
    </div>

    <footer>
        <p>© 2025 𝐊ᴀ𝐰sᴀʀ | Living Life My Way 😎</p>
    </footer>

<script>
    const profileBtn = document.getElementById("profileBtn");
    profileBtn.addEventListener("click", () => {
        alert("প্রোফাইল বাটনে ক্লিক হয়েছে!");
    });

    const buttons = document.querySelectorAll(".buttons button");
    buttons.forEach(btn => {
        btn.addEventListener("click", () => {
            alert(`${btn.innerText} বাটনে ক্লিক হয়েছে!`);
        });
    });
</script>

</body>
</html>