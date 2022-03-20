<template>
  <div class="home">
    <h1> Welcome to Lux </h1>

    <img alt="beam of light and person" src="../assets/noah-buscher-3WZkMfh8zsE-unsplash.jpg">
    <br>
    Photo by <a href="https://unsplash.com/@noahbuscher?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Noah Buscher</a> on <a href="https://unsplash.com/s/photos/light?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
  

    <h2>Lux is a web-based activity to help communities become more aware of their silent identities </h2>
    <br>
    <br>
    <h1> See what others have created </h1>

    <ListOfLuxes :luxes="luxes" />
  </div>
</template>

<script>
import ListOfLuxes from "../components/ListOfLuxes.vue"
export default {
  name: 'HomeView',
  components: {
    ListOfLuxes
  },
  computed: {
    luxes() {
      return this.$root.$data.luxes;
    }
  },
}
</script>

<style scoped>

img {
  max-width: 70vw;
  max-height: 70vh;
}

</style>

