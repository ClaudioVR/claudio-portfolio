<template>
  <div>
    <TheIntro />

    <LazyAboutMe />

    <LazyTheTech />

    <div id="portfolio"></div>
    <LazyThePortfolio />

    <!-- <TheApplications /> -->

    <div id="cv"></div>
    <LazyMyCv />
  </div>
</template>

<script>

export default {
  data() {
    return {

    }
  },
}
</script>
<style scoped>
#portfolio #cv {
  height: 5px;
  width: 100%;
}
</style>
