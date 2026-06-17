
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For My Jeje ❤️</title>
<style>
*{box-sizing:border-box}
body{
margin:0;
font-family:Segoe UI,sans-serif;
background:linear-gradient(135deg,#ffd7e8,#fff5fa,#ffffff);
overflow-x:hidden;
}
#cover{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}
.open-btn{
background:#ff4f95;
color:white;
border:none;
padding:18px 35px;
border-radius:50px;
font-size:22px;
cursor:pointer;
}
.hidden{display:none}
.main{
max-width:900px;
margin:auto;
padding:20px;
}
.card{
background:white;
border-radius:30px;
padding:30px;
box-shadow:0 15px 40px rgba(0,0,0,.15);
}
img{
display:block;
margin:auto;
max-width:280px;
width:90%;
border-radius:25px;
}
h1{text-align:center;color:#ff4f95}
.text{
white-space:pre-line;
line-height:1.9;
font-size:18px;
}
.hearts{
position:fixed;
inset:0;
pointer-events:none;
}
.heart{
position:absolute;
animation:fall linear infinite;
font-size:24px;
}
@keyframes fall{
from{transform:translateY(-120px)}
to{transform:translateY(120vh)}
}
.typebox{
border-left:4px solid #ff4f95;
padding-left:15px;
}
</style>
</head>
<body>

<div class="hearts" id="hearts"></div>

<div id="cover">
<div>
<h1>💗 Happy Birthday My Jeje 💗</h1>
<p>Aku punya sesuatu untuk kamu...</p>
<button class="open-btn" onclick="start()">💌 Buka Hadiah</button>
</div>
</div>

<div id="main" class="main hidden">
<div class="card">
<h1>🎂 Selamat Ulang Tahun Sayang 🎂</h1>
<img src="foto.jpg">
<br>
<div class="typebox">
<div id="typed" class="text"></div>
</div>
</div>
</div>

<script>
const message = `Selamat ulang tahun ya sayang 🥳💗

ga kerasa yaa berawal dari chat yang pura-pura salah kirim itu, sampai akhirnya bisa bawa kita sejauh ini. waktu itu mungkin keliatannya sih memang sangat amat gaje banget yaaa, tapi ternyata malah hal itu lah awal dari sesuatu yang jadi salah satu hal terbaik dalam hidup aku hihi 🥹

kadang aku masih sering senyum-senyum sendiri kalo inget gimana awal mula nya kita, dari yang awalnya cuma chat random, pelan pelan berubah jadi orang yang paling aku tunggu tunggu banget kabarnya setiap detik. lucu banget yaa kalo dipikir pikir mah, makasih yaa kamu udah mau respon chat si pura pura salkir ini hehe.

satu hal yang bikin aku makin sayang sama kamu yaitu cara kamu ngetreat aku. kamu ga pernah bikin aku ngerasa kecil (ya tapi memang aku kecil sih ✌🏻) kamu selalu bikin aku ngerasa dihargai, diperhatiin, dan berarti. hal kaya gitu kedengarannya simpel, tapi buat aku itu sangat amat berarti 💗

makanya di hari ulang tahun kamu ini, aku cuma mau bilang terima kasih kamu udah hadir di dunia ini, dan terima kasih udah ngetreat aku dengan cara yang bikin aku makin cinta sama kamu.

Semoga di tahun ini bisa jadi tahun terbaik bagi kamu, semoga semua hal yang selama ini kamu impikan bisa terkabulkan satu persatu, semoga setiap langkah kamu selalu dipenuhi kebahagiaan, dan setiap hari hari kamu selalu terasa hangat seperti yang selalu kamu kasih ke aku (eakkkk muach)
semoga di umur yang baru ini, kamu selalu bahagia, selalu sehat, dan semoga aku bisa selalu terus ada di sisi kamu nemenin setiap saat

love you yaaa my jeje 💗`;

function start(){
document.getElementById('cover').classList.add('hidden');
document.getElementById('main').classList.remove('hidden');

let i=0;
const target=document.getElementById('typed');
const timer=setInterval(()=>{
target.textContent += message.charAt(i);
i++;
if(i>=message.length) clearInterval(timer);
},18);
}

for(let i=0;i<35;i++){
let h=document.createElement('div');
h.className='heart';
h.innerHTML='💗';
h.style.left=Math.random()*100+'%';
h.style.animationDuration=(6+Math.random()*8)+'s';
h.style.animationDelay=(Math.random()*5)+'s';
document.getElementById('hearts').appendChild(h);
}
</script>

</body>
</html>
