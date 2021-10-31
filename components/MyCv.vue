<template>
  <div>
    <div class="wrapper">
      <div>
        <p
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
        <Timeline />
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
  margin-top: 30px;
  margin-bottom: 200px;
}
@media only screen and (min-width: 768px) {
  .wrapper {
    margin-top: 0px;
  }
}
</style>
