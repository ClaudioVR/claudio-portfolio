<template>
  <div>
    <v-row>
      <v-col cols="12" md="6">
        <TheCube />
      </v-col>
    </v-row>
    <!-- <div class="spacer"></div> -->
    <v-row class="mb-16">
      <v-col cols="12" md="4">
        <top-project-2 />
      </v-col>
      <v-col cols="12" md="4">
        <top-project-1 />
      </v-col>
      <v-col cols="12" md="4">
        <top-project-2 />
      </v-col>
    </v-row>

    <v-divider class="ma-16"></v-divider>

    <v-row>
      <v-col cols="12" sm="5">
        <!-- <bar-chart-component /> -->
        <bubble-chart-component />
      </v-col>
      <v-col cols="12" sm="7">
        <div>
          <h2>Lorem ipsum</h2>
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

    <Timeline />
  </div>
</template>

<script>

export default {

}
</script>
<style scoped>
.spacer {
  height: 100px;
  width: 100%;
}
</style>