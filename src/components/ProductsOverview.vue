<template>
  <div class="cards-container">
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
    <ProductCard />
  </div>
</template>

<script>
import ProductCard from './ProductCard'

export default {
  name: 'ProductCards',
  props: {},
  components: {
    ProductCard
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cards-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
  grid-gap: 1.5rem;
  justify-content: center;
  align-items: center;
  width: 80vw;
}

@media only screen and (max-width: 1024px) {
  .cards-container {
    grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
    grid-gap: 0.8rem;
    padding: 0;
  }
}

@media only screen and (max-width: 768px) {
  .cards-container {
    /* grid-template-columns: repeat(auto-fit, minmax(22rem, 1fr)); */
    grid-gap: 0.6rem;
    padding: 0;
  }
}

@media only screen and (max-width: 600px) {
  .cards-container {
    grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
    grid-gap: 0.4rem;
    padding: 0;
    width: 100%;
  }
}

@media only screen and (max-width: 540px) {
  .cards-container {
    grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr));
    grid-gap: 0.4rem;
    padding: 0;
    width: 100%;
  }
}

@media only screen and (max-width: 420px) {
  .cards-container {
    grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr));
    padding: 0;
  }
}

@media only screen and (max-width: 380px) {
  .cards-container {
    grid-template-columns: repeat(auto-fit, minmax(20rem, 1fr));
    padding: 0;
  }
}
</style>
