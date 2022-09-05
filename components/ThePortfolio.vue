<template>
  <div>
    <v-dialog
      v-model="warningDialog"
      max-width="500px"
      transition="dialog-transition"
    >
      <v-card>
        <v-card-title class="d-flex blue white--text">
          Github repository
          <v-spacer></v-spacer>
          <v-btn color="blue" fab dark depressed small
            ><v-icon>mdi-close</v-icon></v-btn
          >
        </v-card-title>
        <v-card-text class="pt-5">
          <p class="text-body-1">
            Commercial apps are property of AgentOS Ltd of Cardiff (UK). All
            their repositories are thus set to Private.
          </p>
          <p class="text-body-1">
            I can happily provide reference contacts from AgentOS if requested.
          </p>

          <p></p>
        </v-card-text>
      </v-card>
    </v-dialog>
    <div class="wrapper">
      <div>
        <p
          data-aos="fade-down"
          class="text-center text-h2 grey--text text--lighten-2"
        >
          portfolio
        </p>
        <p
          data-aos="fade-down"
          class="text-center font-italic text-h6 mb-12 grey--text text--lighten-2"
        >
          commercial apps
        </p>

        <v-row data-aos="fade-up">
          <v-col
            v-for="project in projects"
            :key="project.name"
            class="d-flex justify-center"
            cols="12"
            md="4"
          >
            <v-card outlined max-width="350">
              <TopProject :image-name="project.image" />
              <v-card-text class="mt-n5">
                <p class="text-center text-h5">{{ project.name }}</p>
                <p class="text-center text-body-1 font-weight-light">
                  {{ project.description }}
                </p>
                <div class="d-flex justify-space-between align-center">
                  <v-btn
                    x-small
                    outlined
                    fab
                    depressed
                    color="black"
                    dark
                    @click="warningDialog = true"
                    ><v-icon>mdi-github</v-icon></v-btn
                  >
                  <v-btn
                    color="blue"
                    dark
                    :disabled="!project.released"
                    small
                    depressed
                    @click="reroute(project.url)"
                  >
                    <p class="my-0">View project</p>
                  </v-btn>
                </div>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
        <div class="d-flex justify-center">
          <v-btn nuxt to="/projects" class="mt-10" color="blue" dark>
            View more projects
          </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      warningDialog: false,
      projects: [
        {
          name: 'negApp',
          description:
            'My first commercial app created for AgentOS. Includes appointment booking system and full email service.',
          image: 'negApp.png',
          released: true,
          url: 'https://agentos.com/negapp/',
        },
        {
          name: 'agentPay',
          description:
            'A commercial PWA created for AgentOS. AgentPay includes live banking, invoicing and a killer dashboard.',
          image: 'agentPay.png',
          released: true,
          url: 'https://agentpay.app/',
        },
        {
          name: 'payAgent',
          description:
            'PayAgent is an online payment app that lets users make secure online payments by card and bank transfer.',
          image: 'payAgent.png',
          released: true,
          url: 'https://agentos.com/payment-app/',
        },
      ],
    }
  },
  methods: {
    reroute(url) {
      window.open(url, '_blank')
    },
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
  margin-top: 600px;
}
@media only screen and (min-width: 768px) {
  .wrapper {
    margin-top: 100px;
  }
}
</style>
