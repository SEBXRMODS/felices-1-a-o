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
    font-family: Arial, sans-serif;
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

/* Pantalla inicio */

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
    font-size:42px;
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
    line-height:1.8;
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

    <h1 style="font-size:80px;">❤️</h1>

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
Hoy cumplimos 1 año y 3 meses, y sinceramente todavía me cuesta encontrar las palabras exactas para explicarte todo lo que siento por ti.
Desde que llegaste a mi vida todo cambió para mejor. Cada día contigo se siente más bonito, más especial y más feliz.
</p>

<p>
Me encanta absolutamente todo de ti. Tus ocurrencias, tu forma de hablar, tu sonrisa y la manera en la que haces que cualquier momento simple se vuelva inolvidable.
Eres esa persona que logra alegrarme incluso en los días difíciles.
</p>

<p>
Cuando veo Takis rojos pienso en ti, porque sé cuánto te gustan.
Cuando escucho hablar de caballos paso fino me acuerdo de lo increíble y elegante que eres.
Y hasta el Tajín me recuerda a ti, porque contigo todo tiene más sabor, más emoción y más vida.
</p>

<p>
Gracias por acompañarme durante este tiempo, por apoyarme, por escucharme y por hacerme sentir amado.
No sabes lo feliz que me hace compartir mi vida contigo.
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
Quiero seguir creando recuerdos contigo, seguir riéndome contigo y seguir viviendo miles de momentos más a tu lado.
Porque si este año y 3 meses han sido tan especiales…
no me imagino lo hermoso que será todo lo que todavía nos falta vivir juntos.
</p>

<p>
Te amo muchísimo mi cachetonchita ❤️
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

    musica.play();

}

/* Video final */

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
