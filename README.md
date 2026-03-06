# letter
letterforyou
<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Letter For Shakib ❤️</title><style>

body{
margin:0;
padding:0;
min-height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#fdfbfb,#ebedee);
font-family:Georgia,serif;
overflow:hidden;
}

.letter-container{
background:white;
padding:50px 40px;
border-radius:10px;
box-shadow:0 20px 40px rgba(0,0,0,0.15);
max-width:600px;
width:90%;
text-align:center;
border-top:5px solid #ff4d4d;
}

.letter-text{
font-size:20px;
line-height:1.8;
color:#444;
min-height:160px;
}

.question{
font-size:28px;
font-weight:bold;
color:#ff4d4d;
margin-top:20px;
margin-bottom:30px;
}

button{
padding:12px 35px;
font-size:18px;
font-weight:bold;
border:none;
border-radius:30px;
cursor:pointer;
margin:10px;
}

#btnYes{
background:#ff4d4d;
color:white;
}

#btnNo{
background:#eee;
}

.success-message{
display:none;
font-size:48px;
font-weight:bold;
color:#ff4d4d;
text-align:center;
}

.heart{
position:fixed;
bottom:-50px;
font-size:30px;
animation:floatUp linear forwards;
}

@keyframes floatUp{
0%{transform:translateY(0);opacity:1;}
100%{transform:translateY(-110vh);opacity:0;}
}

</style></head><body><div class="letter-container" id="mainContainer"><div class="letter-text" id="typedText"></div><div class="question">
Will you be my lifeline, Shakib? ❤️
</div><button id="btnYes">YES</button>
<button id="btnNo">No</button>

</div><div class="success-message" id="successMessage">
I Love You Shakib ❤️
</div><audio id="music" loop>
<source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_3b4c96a7f1.mp3">
</audio><script>

const text="My dearest Shakib... Every moment with you feels special. Your smile lights up my darkest days and your presence makes my world complete. I can't imagine my life without you.";

let i=0;
function typing(){

if(i<text.length){
document.getElementById("typedText").innerHTML+=text.charAt(i);
i++;
setTimeout(typing,40);
}

}

typing();

const btnNo=document.getElementById("btnNo");

function moveButton(){

const w=window.innerWidth;
const h=window.innerHeight;

const x=Math.random()*(w-100);
const y=Math.random()*(h-50);

btnNo.style.position="fixed";
btnNo.style.left=x+"px";
btnNo.style.top=y+"px";

}

btnNo.addEventListener("mouseover",moveButton);
btnNo.addEventListener("touchstart",moveButton);

document.getElementById("btnYes").onclick=function(){

document.getElementById("mainContainer").style.display="none";
document.getElementById("successMessage").style.display="block";

document.getElementById("music").play();

setInterval(function(){

const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤️";

heart.style.left=Math.random()*100+"vw";
heart.style.animationDuration=(Math.random()*3+3)+"s";

document.body.appendChild(heart);

setTimeout(()=>{heart.remove()},6000);

},100);

}

</script></body>
</html>
