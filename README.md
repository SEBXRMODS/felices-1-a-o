<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para mi cachetonchita ❤️</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
font-family:Arial,sans-serif;
overflow-x:hidden;
background:black;
color:white;
}

/* Pantallas */

.pantalla{
min-height:100vh;
width:100%;
display:flex;
justify-content:flex-start;
align-items:center;
flex-direction:column;
text-align:center;
position:relative;
padding:40px 20px;
}

/* Inicio */

#inicio{
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
justify-content:center;
}

/* Carta */

#carta{
background:linear-gradient(135deg,#6a0dad,#b266ff);
display:none;
}

/* Animación */

@keyframes fade{

from{
opacity:0;
transform:translateY(30px);
}

to{
opacity:1;
transform:translateY(0);
}

}

/* Nombre */

.nombre{
font-size:45px;
font-weight:bold;
margin:25px 0;
animation:brillo 2s infinite alternate;
}

/* Contador */

.contador{
font-size:24px;
margin-bottom:25px;
text-shadow:0 0 15px white;
}

/* Texto */

.texto{
max-width:900px;
width:100%;
animation:fade 2s ease;
}

p{
font-size:22px;
line-height:1.9;
margin-bottom:30px;
}

/* Botón */

button{
padding:16px 28px;
font-size:20px;
border:none;
border-radius:25px;
cursor:pointer;
background:white;
color:#6a0dad;
transition:0.3s;
margin-top:25px;
box-shadow:0 0 20px rgba(255,255,255,0.5);
}

button:hover{
transform:scale(1.08);
background:#ffd1dc;
}

/* Slider */

.slider{
width:100%;
max-width:850px;
height:500px;
position:relative;
overflow:hidden;
border-radius:25px;
box-shadow:0 0 30px rgba(255,255,255,0.4);
background:black;
margin-bottom:40px;
}

.slide{
position:absolute;
width:100%;
height:100%;
opacity:0;
transition:opacity 1.5s ease-in-out;
}

.slide img{
width:100%;
height:100%;
object-fit:contain;
}

.slide.activa{
opacity:1;
}

/* Corazones */

.corazon{
position:fixed;
color:red;
animation:flotar 5s linear infinite;
z-index:999;
pointer-events:none;
}

@keyframes flotar{

0%{
transform:translateY(100vh);
opacity:1;
}

100%{
transform:translateY(-10vh);
opacity:0;
}

}

/* Brillo */

@keyframes brillo{

from{
text-shadow:
0 0 10px #fff,
0 0 20px #ff66cc,
0 0 30px #ff66cc;
}

to{
text-shadow:
0 0 20px #fff,
0 0 40px #ff99dd,
0 0 60px #ff99dd;
}

}

/* Responsive */

@media(max-width:768px){

.nombre{
font-size:35px;
}

p{
font-size:18px;
}

.slider{
height:320px;
}

button{
font-size:18px;
padding:14px 22px;
}

.contador{
font-size:18px;
}

}

</style>
</head>

<body>

<!-- Música -->

<audio id="musica" loop>
<source src="cancion.mp3" type="audio/mpeg">
</audio>

<!-- Inicio -->

<div id="inicio" class="pantalla">

<h1 style="font-size:90px;">❤️</h1>

<button onclick="mostrarCarta()">
¿Sabes cuánto te amo?
</button>

</div>

<!-- Carta -->

<div id="carta" class="pantalla">

<!-- FOTOS PRIMERO -->

<div class="slider">

<div class="slide activa">
<img src="foto1.jpg">
</div>

<div class="slide">
<img src="foto2.jpg">
</div>

<div class="slide">
<img src="foto3.jpg">
</div>

<div class="slide">
<img src="foto4.jpg">
</div>

</div>

<!-- CONTADOR -->

<div class="contador" id="contador"></div>

<!-- NOMBRE -->

<div class="nombre">
Para mi cachetonchita ✨
</div>

<!-- TEXTO -->

<div class="texto">

<p>
Hoy cumplimos 1 año y 3 meses, y la verdad no sé ni por dónde empezar para explicarte todo lo que siento por ti, mi cachetonchita. Desde que llegaste a mi vida, todo ha sido diferente, más bonito, más especial. Eres esa persona que con solo un mensaje o una sonrisa logra cambiar mi día por completo y hacerme sentir feliz incluso en los momentos difíciles.
</p>

<p>
Me encanta todo de ti, desde las cosas pequeñas hasta las que te hacen única. Me gusta pensar en ti cuando veo unos Takis rojos e imaginarte feliz disfrutándolos. Me encanta saber que te gustan los caballos paso fino, porque siento que tienen esa elegancia y fuerza que también hay en ti. Y hasta algo tan simple como el Tajín me recuerda a ti, porque contigo todo tiene más sabor, más emoción y más vida.
</p>

<p>
Gracias por estar conmigo, por apoyarme, por entenderme y por compartir tantos momentos a mi lado. Gracias por escucharme, por hacerme reír y por demostrarme cada día que contigo todo vale la pena. No todo es perfecto, pero cuando estoy contigo cualquier problema se siente más pequeño.
</p>

<p>
Cada día a tu lado me enseña lo mucho que te amo y lo importante que eres para mí. A veces me pongo a pensar en todo lo que hemos vivido juntos durante este año y 3 meses, y sinceramente no cambiaría nada. Cada recuerdo contigo se volvió especial para mí: las conversaciones, las risas, los momentos simples y todas esas pequeñas cosas que hacen que nuestra historia sea tan bonita.
</p>

<p>
Quiero que sigamos sumando meses, recuerdos y sueños juntos. Quiero seguir abrazándote, seguir haciendo recuerdos contigo y seguir construyendo una historia que nunca termine. Porque si este 1 año y 3 meses ha sido así de especial, no me imagino todo lo hermoso que todavía nos falta por vivir.
</p>

<p>
Y aunque a veces no encuentre las palabras perfectas para demostrarte todo lo que siento, sí tengo claro algo: eres una de las mejores cosas que me han pasado en la vida y no quiero perderte jamás.
</p>

<p>
Te amo muchísimo ❤️
</p>

</div>

<!-- BOTÓN FINAL -->

<button onclick="irVideo()">
¿Lista para vivir los mejores momentos de tu vida conmigo?
</button>

</div>

<script>

/* Mostrar carta */

function mostrarCarta(){

document.getElementById('inicio').style.display='none';

document.getElementById('carta').style.display='flex';

const musica = document.getElementById("musica");

musica.volume = 0.5;

musica.play();

}

/* Botón */

function irVideo(){

window.location.href =
"https://youtu.be/o_ls8ltVFnw?si=JbD_Koz2Tlv8YjNn";

}

/* Corazones */

function crearCorazones(){

const corazon=document.createElement('div');

corazon.classList.add('corazon');

corazon.innerHTML='❤️';

corazon.style.left=Math.random()*100+'vw';

corazon.style.fontSize=(Math.random()*20+15)+'px';

document.body.appendChild(corazon);

setTimeout(()=>{
corazon.remove();
},5000);

}

setInterval(crearCorazones,300);

/* Contador */

function actualizarContador(){

const inicio = new Date('2025-02-07T00:00:00');

const ahora = new Date();

const diferencia = ahora - inicio;

const dias = Math.floor(diferencia / (1000*60*60*24));

const horas = Math.floor((diferencia / (1000*60*60)) % 24);

const minutos = Math.floor((diferencia / (1000*60)) % 60);

document.getElementById('contador').innerHTML =
`💖 Llevamos juntos ${dias} días, ${horas} horas y ${minutos} minutos 💖`;

}

setInterval(actualizarContador,1000);

actualizarContador();

/* Slider */

const slides = document.querySelectorAll('.slide');

let actual = 0;

setInterval(()=>{

slides[actual].classList.remove('activa');

actual = (actual + 1) % slides.length;

slides[actual].classList.add('activa');

},3000);

</script>

</body>
</html>
