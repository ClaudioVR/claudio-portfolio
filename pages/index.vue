<template>
  <div>
    <v-row>
      <v-col cols="12" sm="5" md="3">
        <bar-chart-component />
      </v-col>
      <v-col cols="12" sm="7" md="9">
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

    <Timeline /> 
  </div>
</template>

<script>
import BarChartComponent from '~/components/BarChartComponent.vue'
export default {
  components: { BarChartComponent },

}
</script>

<style>
</style>