<template>
  <div>
    <div class="wrapper">
      <div>
        <p
          data-aos="fade-down"
          class="text-center text-h2 mb-12 grey--text text--lighten-2"
        >
          the tech
        </p>
        <v-row>
          <v-col
            v-for="tech in techs"
            :key="tech.name"
            class="d-flex"
            cols="12"
            sm="4"
          >
            <v-card data-aos="fade-up" flat>
              <v-card-title primary-title>
                <v-spacer></v-spacer>

                <v-avatar tile size="150">
                  <img
                    :src="require(`../static/images/${tech.image}`)"
                    :alt="tech.name"
                  />
                </v-avatar>
                <v-spacer></v-spacer>
              </v-card-title>
              <v-card-text class="text-center">
                <p class="text-h6">
                  {{ tech.description }}
                </p>
              </v-card-text>
            </v-card>
          </v-col>

          <!-- <v-col class="d-flex justify-center" cols="12" md="4">
            <TheCube />
          </v-col> -->
        </v-row>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      techs: [
        { name: 'adobeXD', description: 'UI and UX debates and design starts with the wireframing. They`re at the base of everything I do.', image: 'adobexd_logo.svg' },
        { name: 'vue', description: 'I`m a Vue.js man. I use it to build SPAs with routing and state and deploy them as PWAs.', image: 'vue_logo.svg' },
        { name: 'amplify', description: 'I leverage the power of AWS Amplify to create NoSQL databases and Lambda functions to run the app.', image: 'amplify_logo.png' }
      ]
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
  justify-content: center;
  margin-top: 100vh;
}
@media only screen and (min-width: 768px) {
  .wrapper {
    margin-top: 100px;
  }
}
</style>
