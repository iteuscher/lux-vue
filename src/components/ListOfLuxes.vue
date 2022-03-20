<template>
<div>
  <div class="wrapper">
    <div class="luxes">
      <div class="lux" v-for="lux in computedObj" :key="lux.id">
        <div class="info">
          <h1>{{lux.luxName}}</h1>
          <p>Created by: <br> {{lux.adminName}}</p>
          <div class="launch">

            <router-link :to="{ name: 'lux', params: { id: lux.id }}">
              <button class="auto">View this Lux</button>  <!-- @click="launch(lux)" -->
            </router-link>
            
          </div>
        </div>
      </div>
    </div>
  </div>
  <button class="showMoreButton" @click="limit += 10">Show more</button>
</div>
</template>

<script>
export default {
  name: 'ListOfLuxes',
  props: {
    luxes: Array
  },
  data(){
    return {
      // object:[], // your original data
      limit: 6 // or any number you wish to limit to
    }
  },
  computed:{
    computedObj(){
      return this.limit ? this.luxes.slice(0,this.limit) : this.luxes
    }
  }
}
</script>

<style scoped>
.showMoreButton
{
  width: 10em;
  margin: 2em;
  height: 2em;
  font-size: 20px;
  /* display: block; */
}

.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.luxes {
  /* margin-top: 20px; */
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.lux {
  margin: 10px;
  margin-top: 10px;
  width: 200px;
}

.lux img {
  border: 2px solid #333;
  height: 250px;
  width: 200px;
  object-fit: cover;
}

.lux .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.info {
  background: #1abc9c;
  color: #000;
  padding: 5px 5px 20px 5px;
  height: 100px;
  border-radius: 10px;
}

.info h1 {
  font-size: 18px;
}

.info h2 {
  font-size: 16px;
}

.info p {
  margin: 0px;
  font-size: 12px;
}


button {
  height: 25px;
  background: rgb(58, 57, 57);
  color: white;
  border: none;
  border-radius: 4px;
}

button:hover {
  background: rgb(7, 135, 233);
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}

.launch {
  padding-top: 5px;
}

.auto {
  margin-left: auto;
}
</style>