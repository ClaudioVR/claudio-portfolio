<template>
  <div>
    <div class="card-wrapper">
      <v-card outlined class="rounded-0" min-width="300" max-width="450">
        <v-card-title class="blue pt-8 pb-12">
          <v-spacer></v-spacer>
          <div class="text-center white--text">
            <p class="text-h4 my-0 font-weight-bold">claudio rescigno</p>
            <p class="text-caption my-0">uk - italy - norway</p>
          </div>
          <v-spacer></v-spacer>
        </v-card-title>
        <div class="d-flex justify-center">
          <v-avatar size="80" class="mx-auto mt-n9">
            <img src="/images/claudio-img.jpg" alt="Claudio" />
          </v-avatar>
          <div class="white-cirlce"></div>
        </div>
        <v-card-text class="pt-5">
          <div class="text-center text-body-1">
            <p>
              I work at
              <a
                href="https://www.linkedin.com/company/agentos-com"
                target="_blank"
                >AgentOS</a
              >
              designing and creating applications for the british real estate
              industry.
            </p>
            <p>
              My background is in humanities, with more than 10 years spent
              working in teaching, recruitment and tourism marketing.
            </p>
            <p>
              After a stint in computer science at university, I veered back
              into front-end development in 2018 and haven't looked back since.
            </p>
          </div>
          <v-divider class="mb-3"></v-divider>
          <v-chip-group
            v-model="selectedChip"
            active-class="blue accent-3 white--text"
            column
          >
            <v-chip @click="goTo('https://uxqb.org/en/')"
              >#uxqbCertified</v-chip
            >

            <v-chip @click="goTo('https://www.adobe.com/products/xd.html')"
              >#adobeXD</v-chip
            >

            <v-chip @click="goTo('https://v3.vuejs.org/')">#vue3</v-chip>

            <v-chip @click="goTo('https://aws.amazon.com/amplify/')"
              >#amplify</v-chip
            >
          </v-chip-group>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedChip: 0
    }
  },
  methods: {
    goTo(url) {
      window.open(url, '_blank')
    }
  }
}
</script>

<style scoped>
#account-icon {
  position: absolute;
  top: 15px;
  right: 15px;
}

.stamp {
  transform: rotate(12deg);
  color: #555;
  font-size: 1.2rem;
  font-weight: 700;
  border: 0.25rem solid #555;
  display: inline-block;
  padding: 0.25rem 1rem;
  text-transform: uppercase;
  border-radius: 1rem;
  font-family: 'Courier';
  -webkit-mask-image: url('https://s3-us-west-2.amazonaws.com/s.cdpn.io/8399/grunge.png');
  -webkit-mask-size: 944px 604px;
  mix-blend-mode: multiply;
}
.sm-stamp-ux {
  color: #d23;
  border: 0.5rem solid #d23;
  -webkit-mask-position: 13rem 6rem;
  transform: rotate(0deg);
  border-radius: 0;
  margin: 15px auto;
}

.stamp-ux {
  color: #d23;
  border: 0.5rem solid #d23;
  -webkit-mask-position: 13rem 6rem;
  transform: rotate(-12deg);
  border-radius: 0;
}
.absolute-stamp {
  position: absolute;
  top: 30px;
  right: 15px;
}
</style>