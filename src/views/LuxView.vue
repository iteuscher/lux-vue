<template>
  <div class="luxView">
    <h1> {{ thisSpecificLux.luxName }} (Lux #{{ $route.params.id }})</h1>

    <h3> Created by: {{ thisSpecificLux.adminName }} | {{ thisSpecificLux.email }} </h3>

    <h3> About {{ thisSpecificLux.luxName }}: {{ thisSpecificLux.luxDescription }}</h3>
    <br>
    <h2> Question 1: </h2>
    <h2> Question 2: </h2>

  </div>
</template>

<script>
export default {
  name: 'LuxView',
  data(){
    return {
      id: this.$route.params.id
    }
  },
  computed:{
    luxes() {
      return this.$root.$data.luxes;
    },
    thisSpecificLux()
    {
      return this.luxes.find(element => element.id == this.id);
      // let title = thislux.adminName;
      // console.log("thisSpecificLux is named: " + title);
      // return title;  
    }
  },
}
</script>