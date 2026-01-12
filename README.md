[index.html](https://github.com/user-attachments/files/24559212/index.html)
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Care Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
<div id="lockScreen" class="lock">
    <h2>💗 Ye page sirf tumhare liye hai</h2>
    <p>Ek chhota sa word likho jo sirf tum jaanti ho</p>
    <input type="password" id="secretInput" placeholder="yahan likho…" />
    <button id="unlockBtn">Open 💌</button>
    <p id="errorMsg" class="error"></p>
</div>

<div class="container">
    <h1>Hlw my red apple fizzzzzz ❤️<br><span id="dailyText"></span></h1>
    <button id="start-btn">Batane ka mann ho to yahan tap karo</button>

    <div id="mood-screen" style="display:none;">
        <button id="happy-btn">😊 Badiya hoon</button>
        <button id="okay-btn">🙂 Thoda-thoda theek</button>
        <button id="sad-btn">😔 Aaj bilkul theek nahi</button>
    </div>
    <div id="message"></div>
</div>

<script>
const correctSecret = "red apply fizz";
const lockScreen = document.getElementById("lockScreen");
const unlockBtn = document.getElementById("unlockBtn");
const secretInput = document.getElementById("secretInput");
const errorMsg = document.getElementById("errorMsg");

unlockBtn.onclick = () => {
  if(secretInput.value.toLowerCase().trim() === correctSecret){
    lockScreen.style.display="none";
  } else {
    errorMsg.innerText="Galat word 🤍";
  }
};

const dailyTexts=[
"Aaj kaisi ho? 🌸",
"Aaj rest lena 🤍",
"Aaj better ya same, dono ok 🙂",
"Aaj bas saans lena kaafi hai",
"Aaj apna khayal rakhna",
"Aaj strong banna zaroori nahi",
"Main yahin hoon 💙"
];
document.getElementById("dailyText").innerText=dailyTexts[new Date().getDay()];

document.getElementById("start-btn").onclick=()=>{
document.getElementById("mood-screen").style.display="block";
};

document.getElementById("happy-btn").onclick=()=>{
document.getElementById("message").innerHTML="Ye sunke achha laga 😊";
};
document.getElementById("okay-btn").onclick=()=>{
document.getElementById("message").innerHTML="Koi baat nahi 🙂";
};
document.getElementById("sad-btn").onclick=()=>{
document.getElementById("message").innerHTML="Main yahin hoon 😔";
};
</script>
</body>
</html>[styles.css](https://github.com/user-attachments/files/24559214/styles.css)

body{font-family:Arial;background:#ffe6f0;text-align:center;padding:20px;}
button{padding:10px 20px;margin:5px;border-radius:20px;border:none;}
.lock{position:fixed;inset:0;background:#fff;display:flex;flex-direction:column;justify-content:center;align-items:center;}
