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
          <p class="text-h6 font-weight-light my-0">{{ job.dates }}</p>
          <p class="font-weight-light my-0">{{ job.length }}</p>
        </template>
        <v-card class="elevation-2">
          <v-card-title class="text-h5">
            <span class="grey--text text--darken-2">{{ job.position }}</span>
            <v-spacer></v-spacer>
            <v-img
              contain
              max-height="auto"
              max-width="80"
              :src="require(`../static/images/${job.image}.png`)"
            ></v-img>
          </v-card-title>
          <v-card-text class="mt-n1">
            <p class="mb-0 font-weight-light text-body-1">
              {{ job.description }}
            </p>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>

    <div class="mt-12 d-flex justify-center">
      <v-btn color="blue" dark @click="rerouteLinkedin">
        <span>find me on Linked</span>
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
          description:
            'Designing and building financial applications for the British real estate industry. Including AgentPay, NegApp, PayAgent and CalmonyApp Beta.',
          dates: 'July 2019 - May 2022',
          length: '2 years 11 months',
          image: 'agentos',
        },
        {
          company: 'VisitOSLO',
          position: 'Project Leader Int. Media',
          description:
            'Managing international media visits and projects in Oslo. I also worked as a Front Office Manager and Information Consultant during my time there.',
          dates: 'April 2013 - March 2018',
          length: '5 years',
          image: 'visitoslo',
        },
      ],
    }
  },
  computed: {
    ifDevice() {
      if (this.$vuetify.breakpoint.smAndDown) return true
      return false
    },
  },
  methods: {
    rerouteLinkedin() {
      const url = 'https://no.linkedin.com/in/claudio-rescigno-6b0531177'
      window.open(url, '_blank')
    },
  },
}
</script>

<style></style>
