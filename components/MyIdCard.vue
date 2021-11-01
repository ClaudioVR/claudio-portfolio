<template>
  <div>
    <div class="card-wrapper">
      <v-card outlined class="rounded-0">
        <v-card-title primary-title>
          <span class="text-h5">claudio rescigno</span>
        </v-card-title>
        <v-card-subtitle>front end developer</v-card-subtitle>
        <v-card-text class="">
          <p class="mb-1 mt-10 mt-sm-0 text-body-1">
            <strong>Nationalities</strong>: UK / ITA / NOR
          </p>
          <p class="my-1 text-body-1"><strong>Framework</strong>: Vue.js</p>
          <p class="my-1 text-body-1">
            <strong>Design tools</strong>: Adobe XD
          </p>
          <p class="my-1 text-body-1">
            <strong>Hobbies</strong>: Backgammon, Aikido, Reading
          </p>
          <p class="my-1 text-body-1"><strong>Favourite food</strong>: Pizza</p>
          <v-card id="account-icon" outlined>
            <v-icon color="grey lighten-3" size="150">mdi-account</v-icon>
          </v-card>
          <span class="d-none d-sm-block stamp stamp-ux absolute-stamp"
            >UXQB Certified</span
          >
          <span class="d-sm-none stamp sm-stamp-ux">UXQB Certified</span>
        </v-card-text>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.card-wrapper {
  /* transform: rotate(5deg); */
}
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