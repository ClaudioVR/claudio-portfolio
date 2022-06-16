<template>
  <div>
    <p class="text-center text-h2 mt-5 mb-8">My projects</p>
    <p
      class="
        font-weight-light
        my-0
        text-center text-h6
        grey--text
        text--darken-2
      "
    >
      Here's a bunch of side projects I've created.
    </p>
    <p
      class="
        font-weight-light
        my-0
        text-center text-h6
        grey--text
        text--darken-2
      "
    >
      From static web pages to web applications with some CSS tricks thrown in
      here and there.
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
            "A working mock version of Dr.Dropin's website. Built as an SPA with Nuxt, powered by Vue.js with full app state.",
          technologies: 'Vue.js Nuxt.js',
          url: 'https://dr-dropin-mock-website.netlify.app/',
        },
        {
          name: 'Skoyen Aikido',
          image: 'skoyen-aikido',
          description:
            'A static website created for my local martial arts club. Includes some particle.js and animate on scroll magic.',
          technologies: 'Vue.js Nuxt.js',
          url: 'https://www.skoyenaikido.no/',
        },
        {
          name: 'NeoTyper',
          image: 'neotyper',
          description:
            "NeoTyper is an online 'green screen' writing platform created using Vue.js. Download your work as a .doc file.",
          technologies: 'Vue.js',
          url: 'https://neotyper.netlify.app/',
        },
        {
          name: 'Fish n Code',
          image: 'fishncode',
          description:
            'A static website for my company created using Nuxt.js. Great for SSR, Nuxt is also an excellent tool for creating static pages on the go.',
          technologies: 'Vue.js Nuxt.js',
          url: 'https://fishncode.netlify.app/',
        },
        {
          name: 'Layer animations',
          image: 'layer-animations',
          description:
            'Art always challenges and inspires my web styling. Watch CSS animations transform this canvass into its respective layers on :hover',
          technologies: 'CSS3',
          url: 'https://claudiovr.github.io/Odd-Tandberg-mockup/',
        },
        {
          name: 'Visit Bøler.com',
          image: 'visit-boler',
          description:
            'A mock tourist office website for Bøler. An experiment in reproducing a page using nothing more than Matrialize and some vanilla CSS.',
          technologies: 'CC3, Materialize CSS',
          url: 'https://claudiovr.github.io/Visit-Boeler-dot-com/',
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
          technologies: 'CSS£, Javascript',
          url: 'https://claudiovr.github.io/Jungle-mockup/',
        },
        {
          name: 'Zen app',
          image: 'zen-app',
          description:
            'A fun side project. The zen app is the perfect tool to help you take 5 minutes to chill out, wherever you are. Go with the chimes.',
          technologies: 'Vue.js',
          url: 'https://zen-app.netlify.app/',
        },
        {
          name: 'CSS art',
          image: 'css-art',
          description:
            'CSS3 animations bringing to life these real-life canvasses by artist Alero Meggison. Art always inspires my front-end design.',
          technologies: 'CSS3',
          url: 'https://claudiovr.github.io/CSS-Art-Alero/',
        },
        {
          name: 'Beer exchange',
          image: 'beer-exchange',
          description:
            'An early project. Prices vary based on the availability of stock. Hit the market crash button to drop prices by ten percent',
          technologies: 'Vue.js',
          url: 'https://vue-beer-exchange.netlify.app/',
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

<style></style>
