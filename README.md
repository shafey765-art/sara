<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For My Saraty 💗</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Segoe UI',Tahoma,sans-serif;
}

body{
background:url('https://i.ibb.co/W4RmYrWH/image.jpg') center center/cover no-repeat fixed;
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
overflow-x:hidden;
}

/* HEARTS */

.hearts{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
pointer-events:none;
z-index:-1;
overflow:hidden;
}

.heart{
position:absolute;
color:#ff4081;
animation:float linear forwards;
}

@keyframes float{
0%{
transform:translateY(100vh) rotate(0deg);
opacity:0;
}
10%{
opacity:1;
}
100%{
transform:translateY(-100px) rotate(360deg);
opacity:0;
}
}

/* CARD */

.card{
background:rgba(255,255,255,.95);
padding:30px;
border-radius:25px;
width:90%;
max-width:650px;
box-shadow:0 15px 50px rgba(0,0,0,.3);
text-align:center;
backdrop-filter:blur(10px);
}

.avatar{
width:170px;
height:170px;
border-radius:50%;
object-fit:cover;
border:6px solid #f8bbd0;
}

.input-box{
padding:14px;
width:85%;
border-radius:12px;
border:2px solid #f48fb1;
font-size:16px;
text-align:center;
margin-top:15px;
}

.btn{
padding:12px 24px;
border:none;
border-radius:12px;
background:#d81b60;
color:white;
font-weight:bold;
cursor:pointer;
margin:5px;
transition:.3s;
}

.btn:hover{
transform:scale(1.08);
box-shadow:0 5px 20px rgba(216,27,96,.4);
}

.hidden{
display:none;
}

/* LOADING */

#loading{
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:white;
display:none;
justify-content:center;
align-items:center;
flex-direction:column;
z-index:9999;
}

.pulse{
font-size:90px;
animation:pulse 1s infinite;
}

@keyframes pulse{
50%{
transform:scale(1.2);
}
}

/* GALLERY */

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
gap:15px;
margin-top:20px;
}

.gallery img{
width:100%;
aspect-ratio:1/1;
object-fit:cover;
border-radius:15px;
border:3px solid #fce4ec;
cursor:pointer;
transition:.3s;
}

.gallery img:hover{
transform:scale(1.05);
}

.read-img{
width:100%;
border-radius:20px;
margin-bottom:20px;
border:3px solid #f8bbd0;
}

/* FULLSCREEN VIEWER */

#viewer{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,.95);
justify-content:center;
align-items:center;
z-index:99999;
}

#viewer img{
max-width:95%;
max-height:95%;
border-radius:20px;
}
</style>
</head>

<body>

<div class="hearts"></div>

<div id="loading">
<div class="pulse">❤️</div>
<h2>Welcome My Saraty ♥️</h2>
</div>

<!-- PASSWORD -->

<div id="lock" class="card">

<img src="https://i.postimg.cc/qttM2cx1/IMG-20260120-WA0060.jpg" class="avatar">

<br><br>

<input
type="password"
id="pass"
class="input-box"
placeholder="Enter Password">

<br><br>

<button class="btn" onclick="check()">
Enter
</button>

<p id="msg" style="color:red;margin-top:10px;"></p>

</div>

<!-- MAIN -->

<div id="gift" class="card hidden">

<h2 style="color:#d81b60;">
Happy Birthday Ya Saraty ♥️🫂
</h2>

<br>

<p style="line-height:1.9;color:#4a148c;">
Before I met you, life was normal...
Then you came and made everything beautiful.
You became part of every happy memory,
every smile and every dream.
</p>

<hr style="margin:20px 0;">

<button class="btn" onclick="showSection('pro')">
Profile
</button>

<button class="btn" onclick="showSection('read')">
Read Me
</button>

<!-- PROFILE -->

<div id="pro" class="hidden">

<div class="gallery">

<img src="https://i.postimg.cc/qttM2cx1/IMG-20260120-WA0060.jpg">

<img src="https://i.postimg.cc/f36WC38B/IMG-20260527-WA0145.jpg">

<img src="https://i.postimg.cc/QBRNmBfz/IMG-20260622-WA0066.jpg">

<img src="https://i.postimg.cc/NyWGDyd8/Screenshot-2026-06-19-02-00-04-573-com-instagram-android-2.jpg">

<img src="https://i.postimg.cc/06L5n6V0/Screenshot-2026-06-19-02-00-23-833-com-instagram-android-2.jpg">

<img src="https://i.postimg.cc/2qPjGq0G/Screenshot-2026-06-19-02-00-29-485-com-instagram-android-2.jpg">

<img src="https://i.postimg.cc/wtSx2twG/Screenshot-2026-06-19-02-01-56-881-com-instagram-android-2.jpg">

</div>

</div>

<!-- READ -->

<div id="read" class="hidden">

<img
src="https://i.postimg.cc/qttM2cx1/IMG-20260120-WA0060.jpg"
class="read-img">

<p style="color:#4a148c;">
And now you've just seen the most beautiful
person God has ever created ♥️
</p>

<br>

<button class="btn" onclick="finalLetter()">
Read More
</button>

</div>

</div>

<!-- VIEWER -->

<div id="viewer" onclick="closeViewer()">
<img id="viewerImg">
</div>

<script>

function check(){

if(document.getElementById('pass').value==="2912026"){

document.getElementById('lock').style.display='none';

document.getElementById('loading').style.display='flex';

setTimeout(()=>{

document.getElementById('loading').style.display='none';

document.getElementById('gift').classList.remove('hidden');

},3000);

}else{

document.getElementById('msg').innerText='Wrong ya Saraty ❤️';

}
}

function showSection(id){

document.getElementById('pro').classList.add('hidden');

document.getElementById('read').classList.add('hidden');

document.getElementById(id).classList.remove('hidden');

}

function finalLetter(){

document.getElementById('read').innerHTML=`

<div style="direction:rtl;text-align:right;line-height:2;color:#4a148c;">

<h2 style="text-align:center;color:#d81b60;">
Happy Birthday My Saraty ♥️
</h2>

<br>

وجودك في حياتي من أجمل نعم ربنا عليا.

<br><br>

أنا بحبك جدًا ♥️🫂

<br><br>

بعيدان نحن ومهما افترقنا<br>
فما زال في راحتيك الأمان<br>
تغيبين عني وكم من قريب<br>
يغيب وإن كان ملء المكان<br>
فلا البعد يعني غياب الوجوه<br>
ولا الشوق يعرف قيد الزمان

<br><br>

<a href="https://vt.tiktok.com/ZSQqedrfD/"
target="_blank">

اضغطي هنا يا سارتي ♥️

</a>

<br><br>

بحبك ♥️

</div>

`;

}

/* FULLSCREEN */

document.addEventListener('click',function(e){

if(e.target.closest('.gallery img')){

document.getElementById('viewer').style.display='flex';

document.getElementById('viewerImg').src=e.target.src;

}

});

function closeViewer(){

document.getElementById('viewer').style.display='none';

}

/* HEARTS */

setInterval(()=>{

let heart=document.createElement('div');

heart.className='heart';

heart.innerHTML='♥';

heart.style.left=Math.random()*100+'vw';

heart.style.fontSize=(15+Math.random()*25)+'px';

heart.style.animationDuration=(5+Math.random()*5)+'s';

document.querySelector('.hearts').appendChild(heart);

setTimeout(()=>{

heart.remove();

},10000);

},500);

</script>

</body>
</html>
