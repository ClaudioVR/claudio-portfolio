<template>
  <div>
    <v-row>
      <v-col v-for="project in projects" :key="project.name" cols="12" md="4">
        <v-card outlined>
          <TopProject :image-name="project.image" />
          <v-card-text class="mt-n5">
            <p class="text-center text-h5">{{ project.name }}</p>
            <p>{{ project.description }}</p>
            <div class="d-flex justify-end">
              <v-btn color="blue" outlined :disabled="!project.released">
                <p v-if="project.released" class="my-0">View project</p>
                <p v-else class="my-0">Awaiting release</p>
              </v-btn>
            </div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <div class="d-flex justify-center">
      <v-btn class="mt-10" color="blue" dark x-large>
        View more projects
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: 'negApp',
          description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Animi recusandaeid suscipit quibusdam ullam accusamus?',
          image: 'negApp.png',
          released: true
        },
        {
          name: 'agentPay',
          description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Animi recusandaeid suscipit quibusdam ullam accusamus?',
          image: 'agentPay.png',
          released: true
        },
        {
          name: 'payAgent',
          description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Animi recusandaeid suscipit quibusdam ullam accusamus?',
          image: 'payAgent.png',
          released: false
        },
      ]
    }
  },
}
</script>

<style>
</style>