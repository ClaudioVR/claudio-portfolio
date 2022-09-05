<template>
  <div>
    <TheIntro />

    <LazyAboutMe id="aboutMe" />

    <LazyTheTech />

    <div id="portfolio"></div>
    <ThePortfolio />

    <!-- <TheApplications /> -->

    <div id="cv"></div>
    <LazyMyCv />
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
}
</script>
<style scoped>
/* #portfolio #cv {
  height: 5px;
  width: 100%;
} */
</style>
