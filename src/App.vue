<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/create">Create</router-link> |
      <router-link to="/present">Present</router-link>
    </nav>
    <router-view/>

     <footer class="text-center text-white fixed-bottom" style="background-color: #212529; padding: 1em; margin-top: 30px; text-align: center;">
      <a style="color: white" target="_blank" href="https://github.com/iteuscher/lux-vue"><h2>Link to GitHub Repo</h2></a>
    </footer>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
