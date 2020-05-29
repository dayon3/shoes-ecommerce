<template>
  <div id="app">
    <NavBar />
    <main>
      <SideBar />
      <ProductsOverview />
    </main>
  </div>
</template>

<script>
import ProductsOverview from './components/ProductsOverview'
import NavBar from './components/NavBar.vue'
import SideBar from './components/SideBar.vue'

export default {
  name: 'App',
  components: {
    ProductsOverview,
    NavBar,
    SideBar
  }
}
</script>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  box-sizing: border-box;
  font-size: 62.5%;
}

body::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  background-color: #f5f5f5;
  border-radius: 0.8rem;
}

body::-webkit-scrollbar {
  width: 0.8rem;
  background-color: #f5f5f5;
}

body::-webkit-scrollbar-thumb {
  background-color: #a0aec0;
}

#app {
  background: whitesmoke;
  color: #555;
  font-family: 'Lato', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  line-height: 1.7;
  min-height: 100vh;
}

main {
  background-color: #d6dfe7;
  min-height: auto;
  /* padding: 3rem; */
  padding: 3rem 4rem 10rem;
  display: flex;
}

@media only screen and (max-width: 1024px) {
  main {
    /* padding: 2rem; */
    padding: 1rem 1.5rem 4.5rem;
  }
}

@media only screen and (max-width: 768px) {
  main {
    padding: 1.5rem;
  }
}

@media only screen and (max-width: 600px) {
  main {
    padding: 1rem;
  }
}

@media only screen and (max-width: 420px) {
  main {
    padding: 0.5rem;
  }
}
</style>
