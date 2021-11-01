<template>
  <div>
    <div class="cube-container">
      <div class="scene">
        <div class="cube">
          <div id="amplify" class="cube__face cube__face--front">
            <p>UI/UX</p>
          </div>
          <div id="vue" class="cube__face cube__face--back">
            <p>Wireframe</p>
          </div>
          <div id="nuxt" class="cube__face cube__face--right"><p>Build</p></div>
          <div id="vuetify" class="cube__face cube__face--left">
            <p>Test</p>
          </div>
          <div id="css" class="cube__face cube__face--top"><p>Release</p></div>
          <div id="js" class="cube__face cube__face--bottom"><p>Repeat</p></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.cube-container {
  width: 100%;
  height: 500px;
  /* height: 70vh; */
  display: flex;
  align-items: center;
  margin-top: -100px;
}

.scene {
  width: 200px;
  height: 200px;
  perspective: 600px;
  margin: 200px auto;
}

.cube {
  width: 100%;
  height: 100%;
  position: relative;
  transform-style: preserve-3d;
  transition: transform 1s;
  transform: translateZ(0);
  animation: rotate 15s ease infinite;
}

.cube p {
  color: #7adcfa;
  font-family: sans-serif;
  font-size: 2rem;
}

/* #vuetify {
  background-image: url('/images/vuetify.png');
  background-size: 100px 100px;
  background-repeat: no-repeat;
  background-position: center center;
}

#vue {
  background-image: url('/images/vue_logo.png');
  background-size: 100px 100px;
  background-repeat: no-repeat;
  background-position: center center;
}

#amplify {
  background-image: url('/images/amplify_logo.png');
  background-size: 100px 100px;
  background-repeat: no-repeat;
  background-position: center center;
}

#js {
  background-image: url('/images/javascript_logo.png');
  background-size: 100px 100px;
  background-repeat: no-repeat;
  background-position: center center;
}

#css {
  background-image: url('/images/html_css_logo.png');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center center;
}

#nuxt {
  background-image: url('/images/nuxt_logo.png');
  background-size: 100px 100px;
  background-repeat: no-repeat;
  background-position: center center;
} */

@keyframes rotate {
  0% {
    transform: rotate3d(0, 1, 1, 0deg);
  }
  20% {
    transform: rotate3d(1, 0, 0, 180deg);
  }
  30% {
    transform: rotate3d(0, 1, 0, 180deg);
  }
  50% {
    transform: rotate3d(0, 1, 0, -90deg);
  }
  60% {
    transform: rotate3d(0, 1, 0, 90deg);
  }
  70% {
    transform: rotate3d(1, 0, 0, 270deg);
  }
  80% {
    transform: rotate3d(1, 0, 0, 90deg);
  }
  90% {
    transform: rotateX(720deg);
  }
  100% {
    transform: rotate3d(0, 1, 1, 0deg);
  }
}

.cube__face {
  position: absolute;
  width: 200px;
  height: 200px;
  opacity: 0.95;
  display: flex;
  justify-content: center;
  align-items: center;
}

.cube__face--front {
  /* Amplify */
  background: #edeaea;
  transform: rotateY(0deg) translateZ(100px);
}
.cube__face--back {
  /* Vue.js */
  /* background: #02ac40; */
  background: #f1f1f1;
  transform: rotateY(180deg) translateZ(100px);
}
.cube__face--right {
  /* react */
  /* background: #008ad2; */
  background: #f1f1f1;
  transform: rotateY(90deg) translateZ(100px);
}
.cube__face--left {
  /* Vuetify */
  /* background: #008ad2; */
  background: #f1f1f1;
  transform: rotateY(-90deg) translateZ(100px);
}
.cube__face--top {
  /* Three amigos */
  /* background: #f37020; */
  background: #f1f1f1;
  transform: rotateX(90deg) translateZ(100px);
}
.cube__face--bottom {
  /* AdobeXD */
  /* background: #f066f4; */
  background: #f1f1f1;
  transform: rotateX(-90deg) translateZ(100px);
}

@media only screen and (min-width: 1024px) {
  .cube-container {
    margin-top: 0px;
  }
}
</style>