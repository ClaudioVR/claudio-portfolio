<template>
  <div>
    <div class="wrapper">
      <div>
        <p
          data-aos="fade-down"
          class="text-center text-h2 mb-12 grey--text text--lighten-2"
        >
          portfolio
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
                <div class="d-flex justify-center">
                  <v-btn
                    color="blue"
                    outlined
                    :disabled="!project.released"
                    small
                    @click="reroute(project.url)"
                  >
                    <p v-if="project.released" class="my-0">View project</p>
                    <p v-else class="my-0">Awaiting release</p>
                  </v-btn>
                </div>
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
        <div class="d-flex justify-center">
          <v-btn
            data-aos="fade-in"
            nuxt
            to="/projects"
            class="mt-10"
            color="blue"
            dark
          >
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
      projects: [
        {
          name: 'negApp',
          description: 'I designed and built this commercial app for AgentOS. It includes a booking system and complete email service.',
          image: 'negApp.png',
          released: true,
          url: 'https://agentos.com/negapp/'
        },
        {
          name: 'agentPay',
          description: 'A commercial PWA I designed and created for AgentOS. AgentPay includes live banking and invoicing.',
          image: 'agentPay.png',
          released: true,
          url: 'https://agentpay.app/'
        },
        {
          name: 'payAgent',
          description: 'PayAgent is an online payment platform. It allows users to make online payments in a fast and secure manner.',
          image: 'payAgent.png',
          released: false,
          url: ''
        },
      ]
    }
  },
  methods: {
    reroute(url) {
      window.open(url, '_blank')
    }
  }
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