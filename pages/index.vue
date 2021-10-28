<template>
  <div>
    <TheIntro />

    <p class="text-center text-h2 mb-md-n16">Tech</p>
    <v-row>
      <v-col class="d-flex align-center" cols="12" md="6">
        <div>
          <p class="text-body-1">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae,
            distinctio. Ex nulla vero iusto, laudantium perspiciatis ad harum
            obcaecati modi! Quod fugiat architecto sequi eius molestiae
            reprehenderit fuga aperiam voluptates.
          </p>
          <p class="body-1">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium
            fugiat quo quia autem deleniti? Veritatis!
          </p>
        </div>
      </v-col>
      <v-col class="" cols="12" md="6">
        <TheCube />
      </v-col>
    </v-row>

    <p class="text-center text-h2 mb-12">Portfolio</p>
    <TopThreeProjects />

    <v-divider class="ma-16"></v-divider>

    <v-row>
      <v-col cols="12" sm="5">
        <!-- <bar-chart-component /> -->
        <bubble-chart-component />
      </v-col>
      <v-col cols="12" sm="7">
        <div>
          <p class="text-h2 mb-1">Applications</p>
          <p class="text-h6 font-weight-regular mt-0">
            Vue.js - Vuetify - Charts.js
          </p>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque
            voluptate laudantium itaque quos tempore necessitatibus pariatur,
            quas atque porro cumque facere reiciendis non est rem laborum
            asperiores molestias minus. Optio tempora laudantium animi nobis
            quod delectus incidunt nisi. Iste, ut temporibus animi veritatis
            expedita vel provident. Recusandae quos inventore in.
          </p>
        </div>
      </v-col>
    </v-row>

    <v-divider class="ma-16"></v-divider>

    <MyCv />
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
.spacer {
  height: 100px;
  width: 100%;
}
</style>