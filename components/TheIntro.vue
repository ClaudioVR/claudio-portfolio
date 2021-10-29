<template>
  <div>
    <div class="wrapper d-flex align-center justify-center">
      <div>
        <div class="d-sm-flex align-center">
          <v-avatar size="250">
            <img src="/images/claudio-img.jpg" alt="John" />
          </v-avatar>
          <div
            class="
              text-center
              mt-5 mt-sm-0
              text-sm-left
              ml-sm-5
              grey--text
              text--darken-3
            "
          >
            <p class="my-0 text-h4">claudio rescigno</p>
            <p class="mt-3 mb-0 text-h6">front end developer</p>
            <p class="my-0">oslo, norway</p>
            <div class="languages d-flex justify-center justify-sm-start mt-5">
              <div v-for="lang in languages" :key="lang" class="">
                <v-avatar size="30" color="red" class="mr-3">
                  <img
                    :src="`https://flagcdn.com/w160/${lang}.png`"
                    alt="alt"
                  />
                </v-avatar>
              </div>
            </div>
          </div>
        </div>
        <div class="d-flex justify-center chevron">
          <v-btn color="grey lighten-3" text>
            <v-icon x-large>mdi-chevron-down</v-icon>
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
      languages: [
        "gb",
        "it",
        "no",
        "es",
        "fr"
      ]
    }
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