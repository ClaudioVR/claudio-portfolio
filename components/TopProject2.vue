<template>
  <div class="computer-img">
    <img class="agent" src="/images/visitoslo.png" alt="" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [

      ]
    }
  },
}
</script>
<style scoped>
.computer-img {
  height: 300px;
  width: 100%;
  position: relative;
  top: 0;
  left: 0;
  background-image: url('https://www.bebold.ch/img/home/macbook-white.png');
  background-size: contain;
  background-position: center center;
}
.agent {
  position: absolute;
  top: 110px;
  left: 50%;
  transform: translate(-50%);
  height: auto;
  width: 100px;
}
</style>



