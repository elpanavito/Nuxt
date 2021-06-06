<template>
  <div>
    <div class="container">

        <h1 class="title">
          LOS ANDES VENEZOLANOS
        </h1>
        <img class="portada" src="~/assets/portada.gif" alt="">

    </div>

    <div class="container1">
      <div class="info">
          <h5>LOS ANDES <br> VENEZOLANOS</h5>
          <p>La Región Andina es una de las regiones político-administrativas organizadas en 1969 en Venezuela para su descentralización. Como su nombre indica, comprende los estados andinos (Táchira, Mérida y Trujillo), sin embargo, a estos se agregan algunas partes del Estado Barinas y el Municipio Páez del Estado Apure ambos mayormente llaneros, debido al hecho que la gran mayoría de su población se encuentra cerca del piedemonte andino. Con una extensión de 77 820 km² y una población aproximada de 4 260 000 habitantes.</p>
      </div>
    </div>
    <!--container2 amarillo-->
    <div class="container2">
        <!--<span id="animate1">Contenedor 2</span>-->
        <div class="map_sect">

          <div class="text">
            <ul class="spec">
              <p>Zona//Estado</p>
              <h3>Táchira, Mérida</h3>
            </ul>

            <ul class="spec">
              <p>Habitantes</p>
              <h3>San Cristóbal</h3>
            </ul>

            <ul class="spec">
              <p>Altitud</p>
              <h3>4.978 m.s.n.m</h3>
            </ul>

            <ul class="spec">
              <p>Superficie</p>
              <h3>77.820 km2</h3>
            </ul>

          </div>

          <ul id="trigger1" class="map">
            <img id="reveal1" src="~/assets/map_1.png" alt="map">
          </ul>
        </div>
    </div>
    <!--container3 negro-->
    <div class="container3">
      <h1 class="touch">Sitios</h1>
        <div id="animate2" class="roll">
          <img id="reveal2" class="tour" src="~/assets/tour_2.png" alt="lobatera">
          <img id="reveal2" class="tour" src="~/assets/tour.png" alt="mukumbari">
          <img id="reveal2" class="tour" src="~/assets/tour_3.png" alt="observatorio">

        </div>
    </div>
    <!--container4 rojo-->
    <div class="container4">
      <h1>COOL FACT</h1>
      <div class="content_box">
          <div class="content">
            <ul class="pastel_text">
              <h5>Los pastelitos andinos</h5>
              <p>Estos pastelitos Andinos o pastelitos de harina de trigo, crujientes y rellenos, son una de las delicias más reconocidas de los Andes venezolanos. Están muy bien para desayunar junto con un chocolate caliente espeso o para la merienda. Si quieres otra opcion mas fuerte prueba unas ricas empanadas de queso , esta en ti probar cualquiera de esta dos opciones para disfrutar de los mejores desayunos cada mañana.</p>
            </ul>

            <ul class="fotos">
              <img id="animatestar" class="photo_one" src="~/assets/star.png" alt="star">
              <img class="photo_two" src="~/assets/pastel.png" alt="pastel">
              <img id="reveal3" class="photo_three" src="~/assets/pastel_1.png" alt="pastel">

            </ul>
        </div>
      </div>

    </div>
    <!--container5-->
    <div class="container5">
      <div class="content5">
        <h1>Gracias por ver</h1>
        <img class="chigui" src="~/assets/ending.png" alt="">
      </div>
    </div>

  </div>
</template>

<script>
export default {
  mounted(){
    const controller = new this.$scrollmagic.Controller();

    var scene = new this.$scrollmagic.Scene({ triggerElement: '.container2' })
      // trigger a TweenMax.to tween
      .setTween(".spec", 0.5, { scale: 1.15})
      .addTo(controller);

    var scene2 = new this.$scrollmagic.Scene({ triggerElement: '#trigger1',
			triggerHook: 1, // show, when scrolled 10% into view
			duration: "100%", // hide 10% before exiting view (80% + 10% from bottom)
			offset: 50 // move trigger to center of element })
      // trigger a TweenMax.to tween
      })

      .setClassToggle("#reveal1", "visible") // add class to reveal
			//.addIndicators() // add indicators (requires plugin)
			.addTo(controller);

    var scene3 = new this.$scrollmagic.Scene({ triggerElement: '.container3', duration:1000, 
    	triggerHook: 0.9, // show, when scrolled 10% into view
			duration: "100%", // hide 10% before exiting view (80% + 10% from bottom)
			offset: 50,
      })
      .setTween(".touch", 0.5, { scale: 0.8})
      .setClassToggle("#reveal2", "visible") // add class to reveal
      .addTo(controller);

    var scene4 = new this.$scrollmagic.Scene({ triggerElement: '.container4', duration: 900 })
      // trigger a TweenMax.to tween
      .setTween("#animatestar", 0.5, { rotation: 360})
      .setClassToggle("#reveal3", "visible") // add class to reveal
      .addTo(controller);
      // add indicators (requires plugin)
      //.setTween("#animate2", 0.5, {backgroundColor: "white"})

  }
}

</script>


<style lang="scss">
html {
  overflow-x: hidden;
}
div {
  color: #ffffff;
}
h1 {
  font-size: 144pt;
  line-height: 180px;
}

h3 {
  font-size: 72pt;
}

h5 {
  font-size: 36px;
}

p {
  font-family: 'roboto';
  font-size: 18pt;
}

.container1 {
  background: #222222;
  display: flex;
  justify-content: center;
  width: 100%;
  .info {
    display: grid;
    grid-template-columns:repeat(3, 1fr);
    height: 343px;
    padding: 2rem;
    padding-top: 2rem;
    grid-template-areas: 
    "h5 p p";
    h5 {
      grid-area: h5;
      margin-top: 5rem;
      margin-left: 11rem;
      margin-right: 3rem;
    }
    p {
      grid-area: p;
      margin-top: 1rem;
      max-width: 60ch;
    }
  }
}
 	#reveal1 {
		opacity: 0;
		-webkit-transform: scale(0.9);
			 -moz-transform: scale(0.9);
				-ms-transform: scale(0.9);
				 -o-transform: scale(0.9);
						transform: scale(0.9);
		-webkit-transition: all 350ms ease-in-out;
			 -moz-transition: all 350ms ease-in-out;
				-ms-transition: all 350ms ease-in-out;
				 -o-transition: all 350ms ease-in-out;
						transition: all 350ms ease-in-out;
	}
	#reveal1.visible {
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #0C3DBD;
 
    h1 {
      position: relative;
      z-index: 2;
    color: #ffffff;
    top: 70px;
    left: 830px;
  }
  .portada {
    position: relative;
    z-index: 0;
    right: 630px;
    height: 720px;
  }
}
.container2 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  background: #f8bc48;
  object-fit: cover;
  .map_sect {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    .text {
      margin-top: 4rem;
      position: relative;
      padding-left: 4rem;
      .spec {
        margin-left: 2rem;

        H3 {
          margin-bottom: 1rem;
        }
      }
      .map {
        img {
          object-fit: cover;
          width: 780px;
        }
        }
    }
  }
}

 	#reveal2 {
		opacity: 0;
		-webkit-transform: scale(0.9);
			 -moz-transform: scale(0.9);
				-ms-transform: scale(0.9);
				 -o-transform: scale(0.9);
						transform: scale(0.9);
		-webkit-transition: all 350ms ease-in-out;
			 -moz-transition: all 350ms ease-in-out;
				-ms-transition: all 350ms ease-in-out;
				 -o-transition: all 350ms ease-in-out;
						transition: all 350ms ease-in-out;
	}
	#reveal2.visible {
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}

.container3 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #222222;
  padding-bottom: 1rem;
  .touch {
    font-size: 80pt;
    line-height: 6rem;
  }
  .roll {
    display: flex;
    justify-content: space-evenly ;
    .tour {
      margin: 1rem;
      height: 340px;
      width: 340px;
    }
  }
}

.container4 {
  margin: 0 auto;
  min-height: 100vh;
  background: #F34040;
  h1 {
    display: flex;
    justify-content: center;
    margin-bottom: .7rem;
  }
  .content_box {
    display: flex;
    justify-content: center;
  }
  .content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    padding: 7.5rem;
    background: #222222;
    width: 95%;
    height: 630px;
    .pastel_text {
      width: 60ch;
    }
    .fotos {
      display: flex;
      position: relative;
      .photo_one {
        position: relative;
        width: 600px;
        height: 600px;
        left: 50px;
        bottom: 110px;
      }
      .photo_two {
        height: 400px;
        width: 400px;
        position: relative;
        right: 290px;
        bottom: 30px;
      }
      .photo_three {
        height: 350px;
        width: 350px;
        position: relative;
        right: 400px;
        bottom: 0px;
      }
    }
    h5 {
      margin-bottom: 1rem;
    }

  }
}

 	#reveal3 {
		opacity: 0;
		-webkit-transform: scale(0.9);
			 -moz-transform: scale(0.9);
				-ms-transform: scale(0.9);
				 -o-transform: scale(0.9);
						transform: scale(0.9);
		-webkit-transition: all 350ms ease-in-out;
			 -moz-transition: all 350ms ease-in-out;
				-ms-transition: all 350ms ease-in-out;
				 -o-transition: all 350ms ease-in-out;
						transition: all 350ms ease-in-out;
	}
	#reveal3.visible {
		opacity: 1;
		-webkit-transform: none;
			 -moz-transform: none;
				-ms-transform: none;
				 -o-transform: none;
						transform: none;
	}

.container5 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #0C3DBD;
  .chigui {
    width: 110%;
    position: relative;
    bottom: 180px;
    left: 320px;
    padding: 0;
    margin: 0;
    opacity: 90%;
    mix-blend-mode: multiply;
  }
  h1 {
    position: relative;
    z-index: 2;
  }
}


.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

@media screen and (max-width: 1100px) {
  .container {
    width: 80%;
  }
}
</style>
