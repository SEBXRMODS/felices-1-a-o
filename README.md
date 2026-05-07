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
      overflow:hidden;
      background:black;
    }

    .pantalla{
      width:100vw;
      height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      flex-direction:column;
      text-align:center;
      position:relative;
    }

    #inicio{
      background:linear-gradient(135deg,#ff9a9e,#fad0c4);
      color:white;
    }

    #carta{
      background:linear-gradient(135deg,#6a0dad,#b266ff);
      color:white;
      display:none;
      overflow-y:auto;
      padding:30px;
      animation:fadeIn 2s ease;
    }

    h1{
      font-size:70px;
      animation:latido 1.5s infinite;
    }

    .nombre-brillante{
      font-size:35px;
      font-weight:bold;
      margin-bottom:20px;
      animation:brilloTexto 2s infinite alternate;
    }

    .contador{
      font-size:22px;
      margin-bottom:20px;
      font-weight:bold;
      text-shadow:0 0 10px white;
      animation:aparecerTexto 2s ease;
    }

    .texto{
      max-width:700px;
      line-height:1.8;
      font-size:20px;
      animation:aparecerTexto 3s ease;
    }

    button{
      padding:15px 25px;
      font-size:18px;
      border:none;
      border-radius:20px;
      cursor:pointer;
      background:white;
      color:#6a0dad;
      margin-top:25px;
      transition:0.3s;
      box-shadow:0 0 15px rgba(255,255,255,0.6);
    }

    button:hover{
      transform:scale(1.1);
      background:#ffd1dc;
    }

    .corazon{
      position:absolute;
      color:red;
      animation:flotar 5s linear infinite;
    }

    .brillo{
      position:absolute;
      width:5px;
      height:5px;
      background:white;
      border-radius:50%;
      animation:brillar 2s infinite alternate;
    }

    .galeria{
      width:100%;
      max-width:700px;
      height:350px;
      margin:25px auto;
      position:relative;
      overflow:hidden;
      border-radius:20px;
      box-shadow:0 0 25px rgba(255,255,255,0.4);
    }

    .galeria img{
      width:100%;
      height:100%;
      object-fit:cover;
      position:absolute;
      opacity:0;
      transition:opacity 1.5s ease;
    }

    .galeria img.activa{
      opacity:1;
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

    @keyframes latido{
      0%,100%{
        transform:scale(1);
      }
      50%{
        transform:scale(1.2);
      }
    }

    @keyframes fadeIn{
      from{
        opacity:0;
        transform:translateY(30px);
      }
      to{
        opacity:1;
        transform:translateY(0);
      }
    }

    @keyframes aparecerTexto{
      from{
        opacity:0;
      }
      to{
        opacity:1;
      }
    }

    @keyframes brillar{
      from{
        opacity:0.2;
        transform:scale(1);
      }
      to{
        opacity:1;
        transform:scale(2);
      }
    }

    @keyframes brilloTexto{
      0%{
        text-shadow:
          0 0 5px #fff,
          0 0 10px #ff66cc,
          0 0 20px #ff66cc;
      }

      100%{
        text-shadow:
          0 0 20px #fff,
          0 0 30px #ff99dd,
          0 0 40px #ff99dd;
      }
    }

  </style>
</head>

<body>

<!-- Música -->
<iframe
  id="musica"
  width="0"
  height="0"
  src=""
  frameborder="0"
  allow="autoplay">
</iframe>

<!-- Pantalla inicial -->
<div id="inicio" class="pantalla">

  <h1>❤️</h1>

  <button onclick="mostrarCarta()">
    ¿Sabes cuánto te amo?
  </button>

</div>

<!-- Carta -->
<div id="carta" class="pantalla">

  <div class="contador" id="contador"></div>

  <div class="texto">

    <div class="nombre-brillante">
      Para mi cachetonchita ✨
    </div>

    <p>
      Hoy cumplimos 1 año y 3 meses, y la verdad no sé ni por dónde empezar para explicarte todo lo que siento por ti, mi cachetonchita.
      Desde que llegaste a mi vida, todo ha sido diferente, más bonito, más especial.
      Eres esa persona que con solo un mensaje o una sonrisa logra cambiar mi día por completo.
    </p>

    <br>

    <p>
      Me encanta todo de ti, desde las cosas pequeñas hasta las que te hacen única.
      Me gusta pensar en ti cuando veo unos Takis rojos, imaginarte feliz disfrutándolos.
      Me encanta saber que te gustan los caballos paso fino, porque siento que tienen esa elegancia y fuerza que también hay en ti.
      Y hasta algo tan simple como el Tajín me recuerda a ti, porque contigo todo tiene más sabor, más emoción.
    </p>

    <br>

    <p>
      Gracias por estar conmigo, por apoyarme, por entenderme y por compartir tantos momentos a mi lado.
      No todo es perfecto, pero contigo todo vale la pena.
      Cada día a tu lado me enseña lo mucho que te amo y lo importante que eres para mí.
    </p>

    <br>

    <p>
      Quiero que sigamos sumando meses, recuerdos y sueños juntos.
      Porque si estos 1 año y 3 meses han sido así de especiales,
      no me imagino todo lo que nos falta por vivir.
    </p>

    <!-- GALERÍA -->
    <div class="galeria">

      <!-- CAMBIA ESTAS FOTOS -->
      <img src="foto 1.jpg" class="activa">
      <img src="foto 2.jpg">
      <img src="foto 3.jpg">
      <img src="foto 4.jpg">

    </div>

    <p>
      <strong>
        Te amo mucho ❤️
      </strong>
    </p>

    <button onclick="irVideo()">
      ¿Lista para vivir los mejores momentos de tu vida conmigo?
    </button>

  </div>

</div>

<script>

  function mostrarCarta(){

    document.getElementById('inicio').style.display = 'none';

    document.getElementById('carta').style.display = 'flex';

    // Música
    document.getElementById("musica").src =
    "https://www.youtube.com/embed/vbHU5vUwS-A?autoplay=1&loop=1&playlist=vbHU5vUwS-A";

  }

  function irVideo(){

    window.location.href =
    "https://youtu.be/o_ls8ltVFnw?si=JbD_Koz2Tlv8YjNn";

  }

  // Corazones
  function crearCorazones(){

    const corazon = document.createElement('div');

    corazon.classList.add('corazon');

    corazon.innerHTML = '❤️';

    corazon.style.left = Math.random()*100 + 'vw';

    corazon.style.fontSize =
    (Math.random()*20 + 10) + 'px';

    document.body.appendChild(corazon);

    setTimeout(()=>{
      corazon.remove();
    },5000);

  }

  // Brillos
  function crearBrillos(){

    const brillo = document.createElement('div');

    brillo.classList.add('brillo');

    brillo.style.left = Math.random()*100 + 'vw';

    brillo.style.top = Math.random()*100 + 'vh';

    document.body.appendChild(brillo);

    setTimeout(()=>{
      brillo.remove();
    },2000);

  }

  setInterval(crearCorazones,300);

  setInterval(crearBrillos,200);

  // CONTADOR
  function actualizarContador(){

    // CAMBIA ESTA FECHA
    const inicio =
    new Date('2025-02-07T00:00:00');

    const ahora = new Date();

    const diferencia = ahora - inicio;

    const dias =
    Math.floor(diferencia / (1000*60*60*24));

    const horas =
    Math.floor((diferencia / (1000*60*60)) % 24);

    const minutos =
    Math.floor((diferencia / (1000*60)) % 60);

    document.getElementById('contador').innerHTML =
    `💖 Llevamos juntos ${dias} días, ${horas} horas y ${minutos} minutos 💖`;

  }

  setInterval(actualizarContador,1000);

  actualizarContador();

  // GALERÍA
  const fotos =
  document.querySelectorAll('.galeria img');

  let fotoActual = 0;

  setInterval(()=>{

    fotos[fotoActual].classList.remove('activa');

    fotoActual =
    (fotoActual + 1) % fotos.length;

    fotos[fotoActual].classList.add('activa');

  },3000);

</script>

</body>
</html>
