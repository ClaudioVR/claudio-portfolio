<template>
  <div>
    <div class="wrapper d-flex align-center justify-center">
      <div v-if="showContent">
        <div class="d-sm-flex align-center">
          <v-avatar
            data-aos="fade-in"
            size="300"
            @mouseover="hover = true"
            @mouseout="hover = false"
          >
            <!-- <img src="/images/claudio-img.jpg" alt="Claudio image" /> -->
            <img src="/images/claudioAvatar.png" alt="Claudio image" />
          </v-avatar>
          <div
            class="text-center mt-5 mt-sm-0 text-sm-left ml-sm-10 grey--text text--darken-3"
          >
            <p class="my-0 text-h4" data-aos="fade-up">claudio rescigno</p>
            <p
              class="mt-3 mb-0 text-h6"
              data-aos="fade-up"
              data-aos-delay="200"
            >
              front end developer
            </p>
            <p class="my-0" data-aos="fade-up" data-aos-delay="400">
              oslo, norway
            </p>
            <!-- <div
              data-aos="fade-in"
              data-aos-delay="600"
              class="languages d-flex justify-center justify-sm-start mt-5"
            >
              <div v-for="lang in languages" :key="lang" class="">
                <v-avatar size="30" color="red" class="mr-3">
                  <img
                    :src="`https://flagcdn.com/w160/${lang}.png`"
                    alt="alt"
                  />
                </v-avatar>
              </div>
            </div> -->
          </div>
        </div>
        <div class="d-flex justify-center chevron">
          <v-btn nuxt to="/#aboutMe" color="grey lighten-3" text>
            <v-icon x-large>mdi-chevron-down</v-icon>
          </v-btn>
        </div>
      </div>
      <div v-else class="text-center">
        <v-progress-circular
          :size="50"
          color="primary"
          indeterminate
        ></v-progress-circular>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showContent: false,
      languages: ['gb', 'it', 'no', 'es', 'fr'],
    }
  },
  mounted() {
    this.showContent = true
  },
}
</script>

<style scoped>
.wrapper {
  height: calc(100vh - 64px);
  width: 100%;
  position: relative;
}
.chevron {
  position: absolute;
  bottom: 100px;
  left: 50%;
  transform: translateX(-50%);
}
</style>
