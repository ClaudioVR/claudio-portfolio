<template>
  <div>
    <v-timeline :dense="ifDevice" class="ml-n5 ml-sm-0">
      <v-timeline-item
        v-for="(job, i) in jobs"
        :key="i"
        color="blue lighten-2"
        small
      >
        <template #opposite>
          <span class="text-h6 font-weight-light">{{ job.dates }}</span>
        </template>
        <v-card class="elevation-2">
          <v-card-title class="text-h5">
            {{ job.position }}
            <v-spacer></v-spacer>
            <v-img
              contain
              max-height="auto"
              max-width="80"
              :src="require(`../static/images/${job.image}.png`)"
            ></v-img>
          </v-card-title>
          <v-card-text class="mt-n1">
            <p class="mb-0">{{ job.description }}</p>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>

    <div class="mt-12 d-flex justify-center">
      <v-btn color="blue" dark @click="rerouteLinkedin">
        <span>More about me on Linked</span>
        <v-icon>mdi-linkedin</v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          company: 'AgentOS',
          position: 'Front End Developer',
          description: 'Designing and building financial applications for the British real estate industry. These include AgentPay, NegApp and the PayAgent applications.',
          dates: 'Aug 2019 - Present',
          image: 'agentos'
        },
        {
          company: 'VisitOSLO',
          position: 'Project Leader Int. Media',
          description: 'Managing international media visits and projects in Oslo. I also worked as a Front Office Manager and Information Consultant during my time there.',
          dates: '5 Years',
          image: 'visitoslo'
        },
      ],

    }
  },
  computed: {
    ifDevice() {
      if (this.$vuetify.breakpoint.smAndDown) return true
      return false
    }
  },
  methods: {
    rerouteLinkedin() {
      const url = 'https://no.linkedin.com/in/claudio-rescigno-6b0531177'
      window.open(url, '_blank')
    }
  }
}
</script>

<style>
</style>