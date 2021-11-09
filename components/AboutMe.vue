<template>
  <div>
    <div class="wrapper">
      <div class="inner-wrapper">
        <p
          data-aos="fade-down"
          class="text-center text-h2 mb-12 grey--text text--lighten-2"
        >
          about me
        </p>
        <v-row>
          <v-col cols="12" sm="5">
            <img
              data-aos="fade-right"
              height="auto"
              width="100%"
              src="about-me.svg"
              alt="Claudio"
            />
          </v-col>
          <v-col cols="12" sm="7">
            <div
              data-aos="fade-left"
              class="
                text-center text-sm-left text-h6
                font-weight-regular
                text--grey text--darken-2
              "
            >
              <p>
                I work remotely from Oslo for
                <a
                  class="orange--text text-decoration-none"
                  href="https://www.linkedin.com/company/agentos-com"
                  target="_blank"
                  >AgentOS</a
                >
                designing and creating applications for the british real estate
                industry.
              </p>
              <p>
                My background is in humanities, with more than 10 years spent
                working in teaching, recruitment and tourism marketing.
              </p>
              <p>
                After a stint in computer science at university, I veered back
                into front-end development in 2018 and haven't looked back
                since.
              </p>
              <p>
                I`m also a
                <span class="blue--text">UXQB certified professional</span> who
                places a great deal of importance on the user journey.
              </p>
            </div>
            <div class="d-flex justify-center justify-sm-end">
              <v-chip
                class="ml-3"
                color="blue"
                dark
                @click="goTo('https://uxqb.org/en/')"
                >#uxqbProfessional</v-chip
              >

              <v-chip
                class="ml-3"
                color="orange"
                dark
                @click="goTo('https://agentos.com/')"
                >#agentos</v-chip
              >

              <!-- <v-chip
                class="ml-3"
                color="orange"
                dark
                @click="goTo('https://v3.vuejs.org/')"
                >#vue3</v-chip
              >

              <v-chip
                class="ml-3"
                color="orange"
                dark
                @click="goTo('https://aws.amazon.com/amplify/')"
                >#amplify</v-chip
              > -->
            </div>
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
  methods: {
    goTo(url) {
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
  margin-top: 500px;
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