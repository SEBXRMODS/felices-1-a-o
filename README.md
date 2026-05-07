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
}

/* Pantallas */

.pantalla{
min-height:100vh;
width:100%;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
text-align:center;
position:relative;
}

/* Inicio */

#inicio{
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
color:white;
}

/* Carta */

#carta{
background:linear-gradient(135deg,#6a0dad,#b266ff);
color:white;
display:none;
padding:30px 20px 80px;
animation:fade 2s ease;
}

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

/* Texto */

.texto{
max-width:850px;
width:100%;
}

.nombre{
font-size:45px;
font-weight:bold;
margin-bottom:20px;
animation:brillo 2s infinite alternate;
}

.contador{
font-size:24px;
margin-bottom:25px;
text-shadow:0 0 15px white;
}

p{
font-size:22px;
line-height:1.9;
margin-bottom:25px;
}

/* Botones */

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
max-width:800px;
height:550px;
position:relative;
margin:40px auto;
overflow:hidden;
border-radius:25px;
box-shadow:0 0 30px rgba(255,255,255,0.4);
background:black;
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

/* Nombre brillante */

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

</style>
</head>

<body>

<!-- Música -->

<audio id="musica" loop preload="auto">
<source src="cancion.mp3" type="audio/mpeg">
</audio>

<!-- Pantalla Inicio -->

<div id="inicio" class="pantalla">

<h1 style="font-size:90px;">❤️</h1>

<button onclick="mostrarCarta()">
¿Sabes cuánto te amo?
</button>

</div>

<!-- Carta -->

<div id="carta" class="pantalla">

<div class="texto">

<div class="contador" id="contador"></div>

<div class="nombre">
Para mi cachetonchita ✨
</div>

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

<!-- Fotos -->

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

<p>
Te amo muchísimo ❤️
</p>

<button onclick="irVideo()">
¿Lista para vivir los mejores momentos de tu vida conmigo?
</button>

</div>

</div>

<script>

/* Mostrar carta */

function mostrarCarta(){

document.getElementById('inicio').style.display='none';

document.getElementById('carta').style.display='flex';

/* Música */

const musica = document.getElementById("musica");

musica.volume = 0.5;

musica.play().catch(() => {

alert("Toca la pantalla otra vez para activar la música ❤️");

});

}

/* Botón final */

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

/* Slider automático */

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
