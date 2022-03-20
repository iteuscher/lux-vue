<template>
  <div class="present">
    <h1>Find and present your Lux</h1>
  
  <div class="searchBar">
    <form onsubmit="event.preventDefault();" role="search">
      <label for="search">Search for your Lux</label>
      <input v-model="searchText" id="search" type="search" placeholder="Search..." autofocus required />
      <button type="submit">Filtering...</button>
    </form>
  </div>

    
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
  data() {
    return {
      searchText: '',
    }
  },
  computed: {
    luxes() {
      return this.$root.$data.luxes.filter(lux => lux.luxName.toLowerCase().search(this.searchText.toLowerCase()) >= 0 );
    }
  }
}
</script>

<style scoped>
:root {
  --rad: .7rem;
  --dur: .3s;
  --color-dark: #2f2f2f;
  --color-light: #fff;
  --color-brand: #1BBC9B;
  --font-fam: "Lato", sans-serif;
  --height: 5rem;
  --btn-width: 6rem;
  --bez: cubic-bezier(0, 0, 0.43, 1.49);
}

.searchBar {
  /* background: #2f2f2f; */
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 20vh;

  box-sizing: border-box;
}


*, *::before, *::after {
  box-sizing: inherit;
}

form {
  position: relative;
  width: 29rem;
  background: #E8EEEF;
  border-radius: .7rem;
}

input, button {
  height: 4rem;
  font-family: var(--font-fam);
  border: 0;
  color: #2f2f2f;;
  font-size: 1.8rem;
}

input[type=search] {
  outline: 0;
  width: 100%;
  background: var(--color-light);
  padding: 0 1.6rem;
  padding-right: 3.1em;
  border-radius: .7rem;
  -webkit-appearance: none;
     -moz-appearance: none;
          appearance: none;
  transition: all .3s var(--bez);
  transition-property: width, border-radius;
  z-index: 1;
  position: relative;
}

button {
  display: none;
  position: absolute;
  top: 0;
  right: 0;
  width: 6.5rem;
  font-weight: bold;
  background: #1BBC9B;
  font-size: 18px;
  border-radius: 0 .7rem .7rem 0;
}

input:not(:-moz-placeholder-shown) {
  border-radius: .7rem 0 0 .7rem;
  width: calc(100% - var(--btn-width));
}

input:not(:-ms-input-placeholder) {
  border-radius: .7rem 0 0 .7rem;
  width: calc(100% - var(--btn-width));
}

input:not(:placeholder-shown) {
  border-radius: .7rem 0 0 .7rem;
  width: calc(100% - var(--btn-width));
}
input:not(:-moz-placeholder-shown) + button {
  display: block;
}
input:not(:-ms-input-placeholder) + button {
  display: block;
}
input:not(:placeholder-shown) + button {
  display: block;
}

label {
  position: absolute;
  clip: rect(1px, 1px, 1px, 1px);
  padding: 0;
  border: 0;
  height: 10px;
  width: 10px;
  overflow: hidden;
}
</style>