<template>
  <div>
    <div class="wrapper">
      <div>
        <p
          data-aos="fade-down"
          class="
            text-center text-h2
            mb-12
            grey--text
            text--lighten-2
            font-weight-light
          "
        >
          curriculum vitae
        </p>

        <Timeline data-aos="fade-in" />
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.wrapper {
  height: calc(100vh - 64px);
  width: 100%;
  display: flex;
  align-items: center;
  margin-top: 100vh;
  margin-bottom: 200px;
}
@media only screen and (min-width: 768px) {
  .wrapper {
    margin-top: 100px;
  }
}
</style>
