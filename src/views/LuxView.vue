<template>
  <div class="luxView">
    <h1>You are viewing: {{ thisSpecificLux.luxName }} (Lux #{{ $route.params.id }})</h1>

    <p> Created by: {{ thisSpecificLux.adminName }} | {{ thisSpecificLux.email }} </p>

    <p> About {{ thisSpecificLux.luxName }}: {{ thisSpecificLux.luxDescription }}</p>

    <p> Question 1: </p>
    <p> Question 2: </p>

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