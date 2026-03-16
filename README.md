<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para Você ❤️</title>

<style>

body{
font-family: Arial;
background: linear-gradient(135deg,#ff9a9e,#fecfef);
margin:0;
text-align:center;
color:#444;
overflow-x:hidden;
}

/* Corações */
.heart{
position:fixed;
bottom:-10px;
font-size:20px;
animation:subir 6s linear infinite;
opacity:0.7;
}

@keyframes subir{
0%{transform:translateY(0)}
100%{transform:translateY(-110vh)}
}

/* Hero */

.hero{
padding:100px 20px;
}

h1{
font-size:40px;
color:#ff2e63;
}

button{
padding:15px 30px;
border:none;
border-radius:30px;
background:#ff2e63;
color:white;
font-size:16px;
cursor:pointer;
}

/* contador */

.contador{
margin-top:30px;
font-size:22px;
background:white;
display:inline-block;
padding:20px;
border-radius:15px;
}

/* carta */

.carta{
margin-top:60px;
}

.envelope{
width:220px;
height:150px;
background:#ff2e63;
margin:auto;
position:relative;
cursor:pointer;
border-radius:5px;
}

.envelope:before{
content:"";
position:absolute;
top:0;
left:0;
border-left:110px solid transparent;
border-right:110px solid transparent;
border-top:75px solid #ff5c8a;
}

.mensagem{
display:none;
background:white;
padding:25px;
border-radius:10px;
margin-top:20px;
max-width:500px;
margin-left:auto;
margin-right:auto;
}

/* mensagens secretas */

.secret{
margin-top:60px;
}

.card{
display:inline-block;
background:white;
padding:20px;
margin:10px;
border-radius:10px;
cursor:pointer;
}

/* presente */

.presente{
margin-top:60px;
background:#ff2e63;
color:white;
padding:30px;
border-radius:20px;
display:inline-block;
}

</style>
</head>

<body>

<div class="hero">

<h1>Para o Amor da Minha Vida ❤️</h1>

<p>A distância só aumenta a certeza de que eu amo você.</p>

<div class="contador">
Saudade há:<br>
<span id="tempo"></span>
</div>

<br><br>

<button onclick="scrollToCarta()">Abrir Surpresa 💌</button>

</div>

<!-- CARTA -->

<div class="carta" id="carta">

<h2>Uma carta para você 💖</h2>

<div class="envelope" onclick="abrirCarta()"></div>

<div class="mensagem" id="msg">

<p>

Desde que você entrou na minha vida tudo ficou mais bonito.  
Mesmo com a distância, você continua sendo a melhor parte do meu dia.  

Cada conversa nossa, cada risada, cada momento… tudo isso faz eu ter mais certeza ainda do quanto você é especial pra mim.

Eu só queria que você soubesse que, independente da distância, do tempo ou de qualquer coisa…  

❤️ **eu sempre vou escolher você.**

</p>

</div>

</div>

<!-- MENSAGENS SECRETAS -->

<div class="secret">

<h2>Mensagens secretas 🤫</h2>

<div class="card" onclick="alert('Você é meu pensamento favorito todos os dias ❤️')">
Abrir 💌
</div>

<div class="card" onclick="alert('Meu lugar favorito sempre vai ser com você 🥰')">
Abrir 💌
</div>

<div class="card" onclick="alert('Estou contando os dias para te abraçar ❤️')">
Abrir 💌
</div>

<div class="card" onclick="alert('Você é a melhor coisa que já aconteceu comigo 💖')">
Abrir 💌
</div>

</div>

<!-- PRESENTE -->

<div class="secret">

<h2>Seu presente 🎁</h2>

<div class="presente">

<h3>Vale Presente de Amor</h3>

<p>Vale por:</p>

<p>❤️ 1 abraço bem apertado  
❤️ 1 dia inteiro juntos  
❤️ muitos beijos  
❤️ e um jantar quando nos encontrarmos</p>

<b>Código:</b>

<p>AMOR-INFINITO</p>

</div>

</div>

<script>

/* contador saudade */

const inicio = new Date("2025-10-12")

function atualizar(){

let agora = new Date()

let diff = agora - inicio

let dias = Math.floor(diff/86400000)

let horas = Math.floor(diff/3600000)%24

let min = Math.floor(diff/60000)%60

let seg = Math.floor(diff/1000)%60

document.getElementById("tempo").innerHTML =
dias+" dias "+horas+"h "+min+"m "+seg+"s"

}

setInterval(atualizar,1000)

/* abrir carta */

function abrirCarta(){
document.getElementById("msg").style.display="block"
}

/* scroll */

function scrollToCarta(){
document.getElementById("carta").scrollIntoView({
behavior:"smooth"
})
}

/* corações */

function coracao(){

let heart = document.createElement("div")

heart.className="heart"

heart.innerHTML="❤️"

heart.style.left=Math.random()*100+"vw"

document.body.appendChild(heart)

setTimeout(()=>{
heart.remove()
},6000)

}

setInterval(coracao,500)

</script>

</body>
</html>
