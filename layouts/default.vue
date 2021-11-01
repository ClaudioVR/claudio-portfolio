<template>
  <v-app dark>
    <v-app-bar hide-on-scroll flat :clipped-left="clipped" fixed app>
      <NuxtLink to="/">
        <v-toolbar-title>
          <span class="ml-5">claudio rescigno</span>
        </v-toolbar-title>
      </NuxtLink>

      <v-spacer />
      <NuxtLink to="#">portfolio</NuxtLink>
      <NuxtLink to="#">cv</NuxtLink>
      <v-btn color="black" icon>
        <v-icon>mdi-facebook</v-icon>
      </v-btn>
      <v-btn color="black" icon>
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>
      <v-btn color="black" icon>
        <v-icon>mdi-github</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container class="px-3">
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
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
