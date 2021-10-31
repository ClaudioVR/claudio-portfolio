<template>
  <div>
    <div class="wrapper">
      <div class="inner-wrapper">
        <p class="text-center text-h2 mb-12 grey--text text--lighten-2">
          about me
        </p>
        <v-row>
          <v-col cols="12" sm="12" md="6">
            <p>
              I work as a front-end developer at
              <a
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
              into front-end development in 2018 and haven't looked back since.
            </p>
          </v-col>
          <v-col cols="12" sm="12" md="6" class="pt-0">
            <MyIdCard />
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