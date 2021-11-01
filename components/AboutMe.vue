<template>
  <div>
    <div class="wrapper">
      <div class="inner-wrapper">
        <p class="text-center text-h2 mb-12 grey--text text--lighten-2">
          about me
        </p>
        <v-row>
          <v-col cols="12" sm="6" offset-sm="3" class="d-flex justify-center">
            <MyIdCard />
          </v-col>
        </v-row>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
}
</script>

<style scoped>
.wrapper {
  height: calc(100vh - 64px);
  width: 100%;
  display: flex;
  align-items: center;
  margin-top: 300px;
}
.inner-wrapper {
  min-width: 100%;
}
@media only screen and (min-width: 768px) {
  .wrapper {
    margin-top: 0px;
  }
}
</style>