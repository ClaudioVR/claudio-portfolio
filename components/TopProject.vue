<template>
  <div>
    <div class="computer-img">
      <img
        class="agent"
        :src="require(`../static/images/${imageName}`)"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  namd: 'topProject',
  props: {
    imageName: {
      type: String,
      default: 'agentos.png'
    },
  }
}
</script>
<style scoped>
.computer-img {
  margin-top: -40px;
  margin-bottom: -35px;
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
  top: 92px;
  left: 50%;
  transform: translate(-50%);
  height: auto;
  width: 169.5px;
  height: 105px;
}
</style>


