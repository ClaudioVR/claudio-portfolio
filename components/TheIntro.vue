<template>
  <div>
    <div class="wrapper d-flex align-center justify-center">
      <div v-if="showContent">
        <div class="logo-wrapper">
          <NameLogo />
        </div>
        <div
          id="secondary-titles"
          class="text-center mt-5 mt-sm-0 ml-sm-10 grey--text text--darken-3"
        >
          <p class="mt-3 mb-0 text-h6">frontend developer</p>
          <p class="my-0">oslo, norway</p>
        </div>
      </div>
      <div v-else class="text-center">
        <v-progress-circular
          :size="50"
          color="primary"
          indeterminate
        ></v-progress-circular>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showContent: false,
      languages: ['gb', 'it', 'no', 'es', 'fr'],
    }
  },
  mounted() {
    this.showContent = true
  },
}
</script>

<style scoped>
.wrapper {
  height: calc(100vh);
  width: 100%;
  /* margin-top: 64px; */
  margin-bottom: 100px;
}

.logo-wrapper {
  height: 300px;
  width: 500px;
  padding: 0 20px;
}

#secondary-titles {
  opacity: 0;
  transform: translateY(100px);
  animation: fadeIn 1s ease 4s forwards;
}

@keyframes fadeIn {
  to {
    opacity: 1;
    transform: translateY(-50px);
  }
}
</style>
