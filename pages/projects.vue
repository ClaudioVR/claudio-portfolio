<template>
  <div>
    <p class="text-center text-h2 mb-12">Portfolio</p>
    <p class="text-center text-h5">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatibus id
      at totam? Earum, nemo inventore!
    </p>
    <div class="d-flex flex-wrap">
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
          <v-btn color="blue" text> View project </v-btn>
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
          name: "NeoTyper",
          image: 'neotyper',
          description: "NeoTyper is an online 'green screen' writing platform created using Vue.js. Download your work as a .doc file.",
          technologies: 'Vue.js'
        },
        {
          name: "Fish n Code",
          image: 'fishncode',
          description: 'A static website for my company created using Nuxt.js. Great for SSR, Nuxt is also an excellent tool for creating static pages on the go.',
          technologies: 'Nuxt.js'
        },
        {
          name: "Layer animations",
          image: 'layer-animations',
          description: 'Art always challenges and inspires my web styling. Watch CSS animations transform this canvass into its respective layers on :hover',
          technologies: 'CSS3'
        },
        {
          name: "Visit Bøler.com",
          image: 'visit-boler',
          description: "A mock tourist office website for Bøler. An experiment in reproducing a page using nothing more than Matrialize and some vanilla CSS.",
          technologies: 'CC3, Materialize CSS'
        },
        {
          name: "JojoJayne.com",
          image: 'jojojayne',
          description: "Created using the Wordpress theme 'Salient'. Perhpas the first and last one built using Worpress.",
          technologies: 'Wordpress'
        },
        {
          name: "Zen app",
          image: 'zen-app',
          description: "A fun side project. The zen app is the perfect tool to help you take 5 minutes to chill out, wherever you are. Go with the chimes.",
          technologies: 'Vue.js'
        },
        {
          name: "Facebook login",
          image: 'facebook-login',
          description: "A non responive exercise in precision as I recreate Facebook's old login page. Good to practice some CSS and Javascript skills.",
          technologies: 'CSS3'
        },
        {
          name: "CSS art",
          image: 'css-art',
          description: "CSS3 animations bringing to life these real-life canvasses by artist Alero Meggison. Art always inspires my front-end design.",
          technologies: 'CSS3'
        },
        {
          name: "Beer exchange",
          image: 'beer-exchange',
          description: "An early project. Prices vary based on the availability of stock. Hit the market crash button to drop prices by ten percent",
          technologies: 'Vue.js'
        },
      ]
    }
  },
}
</script>

<style>
</style>