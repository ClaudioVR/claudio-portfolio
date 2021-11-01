<template>
  <div>
    <div class="wrapper">
      <div>
        <p class="text-center text-h2 mb-md-n16 grey--text text--lighten-2">
          the journey
        </p>
        <v-row>
          <v-col
            class="d-flex align-center justify-space-around"
            cols="12"
            md="8"
          >
            <v-card flat width="30%" class="mt-1">
              <div class="d-flex justify-center">
                <v-avatar tile size="55">
                  <img src="/images/adobexd_logo.svg" alt="adobexd" />
                </v-avatar>
              </div>
              <v-card-text>
                <p class="text-center body-1 mt-2">
                  i use <strong>adobeXD</strong> to create interactive
                  wireframes. ui and ux design are at the base of it all.
                </p>
              </v-card-text>
            </v-card>
            <v-card flat width="30%">
              <div class="d-flex justify-center pt-1">
                <v-avatar tile size="60">
                  <img src="/images/vue_logo.svg" alt="adobexs" />
                </v-avatar>
              </div>
              <v-card-text>
                <p class="text-center body-1">
                  i build the app with <strong>Vue.js</strong> as an SPA with
                  routing and state and deployt it as a PWA.
                </p>
              </v-card-text>
            </v-card>
            <v-card flat width="30%">
              <div class="d-flex justify-center mt-n3">
                <v-avatar size="100">
                  <img src="/images/amplify_logo.png" alt="adobexs" />
                </v-avatar>
              </div>
              <v-card-text>
                <p class="mt-n5 text-center body-1">
                  we leverage <strong>amplify</strong> to create DBs and lambda
                  functions to run and host our apps.
                </p>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col class="" cols="12" md="4">
            <TheCube />
          </v-col>
        </v-row>
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
  margin-top: 300px;
}
@media only screen and (min-width: 768px) {
  .wrapper {
    margin-top: 100px;
  }
}
</style>
