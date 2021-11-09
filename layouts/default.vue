<template>
  <v-app dark>
    <v-app-bar hide-on-scroll flat :clipped-left="clipped" fixed app>
      <NuxtLink to="/">
        <v-toolbar-title>
          <span class="d-sm-none ml-5">cR</span>
          <span class="d-none d-sm-block ml-5">claudio rescigno</span>
        </v-toolbar-title>
      </NuxtLink>

      <v-spacer />
      <NuxtLink to="/#portfolio">portfolio</NuxtLink>
      <NuxtLink to="/#cv">cv</NuxtLink>
    </v-app-bar>
    <v-main>
      <v-container class="px-3">
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer color="primary lighten-1" padless :absolute="!fixed" app>
      <v-row justify="center" no-gutters>
        <div class="d-flex justify-center align-center">
          <v-btn
            dark
            icon
            @click="reRoute('https://www.facebook.com/claudio.rescigno.359')"
          >
            <v-icon>mdi-facebook</v-icon>
          </v-btn>
          <v-btn
            x-large
            dark
            icon
            @click="
              reRoute('https://no.linkedin.com/in/claudio-rescigno-6b0531177')
            "
          >
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
          <v-btn
            dark
            icon
            @click="reRoute('https://github.com/ClaudioVR?tab=repositories')"
          >
            <v-icon>mdi-github</v-icon>
          </v-btn>
        </div>
        <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
          <span>&copy;{{ new Date().getFullYear() }} claudio rescigno</span>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'claudio rescigno'
    }
  },
  methods: {
    reRoute(url) {
      window.open(url, "_blank")
    }
  }
}
</script>
<style scoped>
.v-application a {
  color: black !important;
  text-decoration: none;
  margin-right: 20px;
}
/* .v-application a.nuxt-link-exact-active {
  font-weight: 800;
} */
</style>
