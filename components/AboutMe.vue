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
          <v-col
            cols="12"
            sm="3"
            class="d-flex justify-center"
            data-aos="fade-up"
          >
            <!-- <img
              data-aos="fade-up"
              height="auto"
              width="100%"
              src="about-me.svg"
              alt="Claudio"
            /> -->
            <v-avatar color="" size="300">
              <img src="about-me.svg" alt="Claudio image" />
            </v-avatar>
          </v-col>
          <v-col cols="12" sm="9" class="d-flex align-center">
            <div>
              <div
                data-aos="fade-up"
                class="
                  text-center text-sm-left text-body-1
                  font-weight-light
                  text--grey text--darken-2
                "
              >
                <p>
                  I'm a creative frontend developer with an passion for UX
                  design.
                </p>
                <p>
                  At
                  <a
                    class="orange--text text-decoration-none"
                    href="https://www.linkedin.com/company/agentos-com"
                    target="_blank"
                    >AgentOS</a
                  >
                  I designed and created a number of successful financial
                  applications for the british real estate industry.
                </p>
                <p>
                  My background is in social sceince, with more than 10 years
                  spent working in teaching, recruitment and tourism marketing.
                </p>
                <p>
                  A short stint studying computer science at university fueled
                  my career into front-end development in 2018 and I haven't
                  looked back since.
                </p>
                <p>
                  I`m also a
                  <span class="blue--text">UXQB certified professional</span>
                  who places a great deal of importance on the user journey.
                </p>
              </div>
              <div class="mt-5 d-flex justify-center justify-sm-start">
                <v-chip
                  class=""
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
              </div>
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
    return {}
  },
  methods: {
    goTo(url) {
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
  margin-top: 300px;
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
