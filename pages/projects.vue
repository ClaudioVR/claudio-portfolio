<template>
  <div>
    <p class="text-center text-h2 mt-5 mb-8">Non commercial projects</p>
    <p
      class="font-weight-light my-0 text-center text-h6 grey--text text--darken-2"
    >
      Single page web applications, static websites and some plain old CSS.
    </p>
    <div class="mt-5 d-flex flex-wrap">
      <v-card
        v-for="(project, i) in projects"
        :key="i"
        class="mx-auto my-6"
        max-width="350"
      >
        <v-img
          height="150"
          :src="require(`../static/images/projects/${project.image}.png`)"
        ></v-img>

        <v-card-title>{{ project.name }}</v-card-title>

        <v-card-text>
          <div class="mt-n5 text-subtitle-1">{{ project.technologies }}</div>

          <div class="mt-5">
            {{ project.description }}
          </div>
        </v-card-text>

        <v-divider class="mx-4"></v-divider>

        <v-card-actions>
          <v-btn
            small
            text
            fab
            depressed
            color="black"
            dark
            @click="repoReroute(project)"
            ><v-icon>mdi-github</v-icon></v-btn
          >
          <v-spacer></v-spacer>
          <v-btn color="blue" text @click="reroute(project.url)">
            View project
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: 'Dr.Dropin',
          image: 'dr-dropin',
          description:
            "A responsive copy of Dr.Dropin's website. Built as an SPA with Nuxt, powered by Vue.js with full app state. Book yourself a mock appointment!",
          technologies: 'Vue.js, Nuxt.js, Vuetify',
          url: 'https://dr-dropin-mock-website.netlify.app/',
          repo: 'https://github.com/ClaudioVR/dr-dropin',
        },
        {
          name: 'Admin App',
          image: 'adminApp',
          description:
            'A mock membership administration app for a potential martial arts club, complete with useful statistics.',
          technologies: 'Vue.js, Vuetify',
          url: 'https://member-admin-app.netlify.app/',
          repo: 'https://github.com/ClaudioVR/member-admin-app',
        },
        {
          name: 'Skøyen Aikido',
          image: 'skoyen-aikido',
          description:
            'A static website created for my local martial arts club. Includes some particle.js and animate on scroll magic.',
          technologies: 'Vue.js, Nuxt.js, Vuetify',
          url: 'https://www.skoyenaikido.no/',
        },
        {
          name: 'NeoTyper',
          image: 'neotyper',
          description:
            "NeoTyper is an online 'green screen' writing platform created using Vue.js. Download your work as a .doc file.",
          technologies: 'Vue.js',
          url: 'https://neotyper.netlify.app/',
          repo: 'https://github.com/ClaudioVR/Neo-typewriter',
        },
        {
          name: 'Pure Table',
          image: 'pureTable',
          description:
            'This is a fully functional table with sorting and CRUD actions. It was creted using pure frontend tools.',
          technologies: 'HTML, CSS, Javascript',
          url: 'https://pure-html-css-js-table.netlify.app/',
          repo: 'https://github.com/ClaudioVR/Simple-CSS-table',
        },
        {
          name: 'Kanban board',
          image: 'kanban',
          description:
            "A quick project exploring the possibilties of drag and drop plugins for vue.js app. In this case I've used it to make a Kanban board.",
          technologies: 'Vue.js, Vuetify',
          url: 'https://kan-ban-board.netlify.app/',
          repo: 'https://github.com/ClaudioVR/kanban-board',
        },
        {
          name: 'Fish n Code',
          image: 'fishncode',
          description:
            'A static website for my company created using Nuxt.js. Great for SSR, Nuxt is also an excellent tool for creating static pages on the go.',
          technologies: 'Vue.js, Nuxt.js, Vuetify',
          url: 'https://fishncode.netlify.app/',
          repo: 'https://github.com/ClaudioVR/FishnCode',
        },
        {
          name: 'Vue.js playground',
          image: 'playground',
          description:
            'A testing ground for Vue.js plugins. Drag grids, design football formations, create documents to download and sign your name digitally!',
          technologies: 'Vue.js',
          url: 'https://vue-playgound.netlify.app/',
          repo: 'https://github.com/ClaudioVR/vue-playground',
        },
        {
          name: 'Visit Bøler.com',
          image: 'visit-boler',
          description:
            'A mock tourist office website for Bøler. An experiment in reproducing a page using nothing more than Matrialize and some vanilla CSS.',
          technologies: 'CC3, Materialize CSS',
          url: 'https://claudiovr.github.io/Visit-Boeler-dot-com/',
          repo: 'https://github.com/ClaudioVR/Visit-Boeler-dot-com',
        },
        {
          name: 'JojoJayne.com',
          image: 'jojojayne',
          description:
            "Created using the Wordpress theme 'Salient'. Perhpas the first and last one built using Worpress.",
          technologies: 'Wordpress',
          url: 'http://jojojayne.com/',
        },
        {
          name: 'JUNGLE mock website',
          image: 'jungle-mockup',
          description:
            "Recreating Jungle's homepage with nothing more than some CSS and a little JavaScript to create the menu's modal window",
          technologies: 'CSS3, Javascript',
          url: 'https://claudiovr.github.io/Jungle-mockup/',
          repo: 'https://github.com/ClaudioVR/Jungle-mockup',
        },
        {
          name: 'Zen app',
          image: 'zen-app',
          description:
            'A fun side project. The zen app is the perfect tool to help you take 5 minutes to chill out, wherever you are. Go with the chimes.',
          technologies: 'Vue.js',
          url: 'https://zen-app.netlify.app/',
          repo: 'https://github.com/ClaudioVR/Zen_app',
        },
        {
          name: 'Layer animations',
          image: 'layer-animations',
          description:
            'Art always challenges and inspires my web styling. Watch CSS animations transform this canvass into its respective layers on :hover',
          technologies: 'CSS3',
          url: 'https://claudiovr.github.io/Odd-Tandberg-mockup/',
          repo: 'https://github.com/ClaudioVR/Odd-Tandberg-mockup',
        },
        {
          name: 'CSS art',
          image: 'css-art',
          description:
            'CSS3 animations bringing to life these real-life canvasses by artist Alero Meggison. Art always inspires my front-end design.',
          technologies: 'CSS3',
          url: 'https://claudiovr.github.io/CSS-Art-Alero/',
          repo: 'https://github.com/ClaudioVR/CSS-Art-Alero',
        },
      ],
    }
  },
  methods: {
    reroute(url) {
      window.open(url, '_blank')
    },
    repoReroute(project) {
      if (project.name === 'Skøyen Aikido') {
        alert('The Skøyen Aikido Club repo is private!')
      } else if (project.name === 'JojoJayne.com') {
        alert('JojoJayne.com is a Wordpress project!')
      } else {
        window.open(project.repo, '_blank')
      }
    },
  },
}
</script>

<style></style>
