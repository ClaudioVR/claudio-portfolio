<template>
  <div>
    <div class="wrapper">
      <div>
        <p class="text-center text-h2 mb-12 grey--text text--lighten-2">
          the applications
        </p>
        <v-row>
          <v-col cols="12" sm="8" offset-sm="2" md="5" offset-md="0">
            <bubble-chart-component />
          </v-col>
          <v-col cols="12" sm="12" md="7">
            <div>
              <p
                class="
                  text-h6 text-center text-md-left
                  font-weight-regular
                  mt-0
                "
              >
                Vue.js - Vuetify - Charts.js
              </p>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Doloremque voluptate laudantium itaque quos tempore
                necessitatibus pariatur, quas atque porro cumque facere
                reiciendis non est rem laborum asperiores molestias minus. Optio
                tempora laudantium animi nobis quod delectus incidunt nisi.
                Iste, ut temporibus animi veritatis expedita vel provident.
                Recusandae quos inventore in.
              </p>
            </div>
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
    margin-top: 0px;
  }
}
</style>