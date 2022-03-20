<template>
  <div class="present">
    <h1>Present your Lux</h1>

    
    <ListOfLuxes :luxes="luxes" />
  </div>
</template>

<script>
import ListOfLuxes from "../components/ListOfLuxes.vue"
export default {
  name: 'PresentView',
  components: {
    ListOfLuxes
  },
  // data() {
  //   // return {
  //   //   country: '',
  //   // }
  // },
  computed: {
    luxes() {
      return this.$root.$data.luxes   //products.filter(product => product.country === this.country);
    }
  },
  // methods: {
  //   // select(country) {
  //   //   this.country = country;
  //   // }
  // }
}
</script>