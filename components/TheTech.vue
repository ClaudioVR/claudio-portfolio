<template>
  <div>
    <div class="wrapper">
      <div>
        <p
          data-aos="fade-up"
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
                <p class="text-body-1 font-weight-light">
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
        {
          name: 'adobeXD',
          description:
            'UI and UX debates and designs start with the wireframing. They`re at the base of everything I do.',
          image: 'adobexd_logo.svg',
        },
        {
          name: 'vue',
          description:
            'I`m a Vue.js man. I build SPAs with it, complete with page routing and state. The apps are then deployed as PWAs.',
          image: 'vue_logo.svg',
        },
        {
          name: 'amplify',
          description:
            'I leverage the power of AWS Amplify to create NoSQL databases and Lambda functions to run the apps.',
          image: 'amplify_logo.png',
        },
      ],
    }
  },
}
</script>
<style scoped>
.wrapper {
  margin-top: 100px;
}
</style>
