<template>
  <div>
    <div class="cube-container">
      <div class="scene">
        <div class="cube">
          <div class="cube__face cube__face--front"><p>GraphQL</p></div>
          <div id="vue" class="cube__face cube__face--back"><p>Vue.js</p></div>
          <div class="cube__face cube__face--right"><p>HTML5</p></div>
          <div id="vuetify" class="cube__face cube__face--left">
            <p>Vuetify</p>
          </div>
          <div class="cube__face cube__face--top"><p>CSS3</p></div>
          <div class="cube__face cube__face--bottom"><p>JavaScript</p></div>
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
/* Rotating cube ----------------------- */

.cube-container {
  width: 100%;
  height: 500px;
  /* height: 70vh; */
  display: flex;
  align-items: center;
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
  color: white;
  font-family: sans-serif;
  font-size: 2rem;
}

#vuetify {
  background-image: url('/v.png');
  background-size: 100px 100px;
  background-repeat: no-repeat;
  background-position: center center;
}

@keyframes rotate {
  0% {
    transform: rotate3d(0);
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
    transform: rotate3d(0);
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
  background: #cd004d;
  transform: rotateY(0deg) translateZ(100px);
}
.cube__face--back {
  background: #0cb14b;
  transform: rotateY(180deg) translateZ(100px);
}
.cube__face--right {
  background: #008ad2;
  transform: rotateY(90deg) translateZ(100px);
}
.cube__face--left {
  /* background: #f37020; orange*/
  background: #008ad2;

  transform: rotateY(-90deg) translateZ(100px);
}
.cube__face--top {
  /* background: #6460ac; purples */
  background: #f37020;
  transform: rotateX(90deg) translateZ(100px);
}
.cube__face--bottom {
  background: #fcb712;
  transform: rotateX(-90deg) translateZ(100px);
}

/* /Rotating cube ----------------------- */
</style>