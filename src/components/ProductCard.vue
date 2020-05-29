<template>
  <figure class="card">
    <div class="card__hero">
      <img
        src="../assets/air-jordan-one-turbo-green.jpg"
        alt="Air Jordan One Phantom"
        class="card__img"
      />
    </div>
    <h2 class="card__name">Air Jordan 1 Turbo Green</h2>
    <div class="card__details">
      <p class="card__detail">
        Shoe
      </p>
      <p class="card__detail">
        2 Colors
      </p>
      <p class="card__price">$100</p>
      <a href="#" class="card__link"
        >Read More <span class="emoji-right">&rarr;</span></a
      >
    </div>
  </figure>
</template>

<script>
// import ProductDetail from './ProductDetail'

export default {
  name: 'ProductCard',
  components: {
    // ProductDetail
  }
}
</script>

<style scoped>
.card {
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);
  border: 1px solid rgba(0, 0, 0, 0.15);
}

.card__img {
  width: 100%;
  display: block;
}

.card h2 {
  font-size: 1.8rem;
  padding: 2rem 0 0 2.5rem;
}

.card__details {
  padding: 0 2.5rem 2rem;
}

.card__detail {
  font-size: 1.4rem;
}

.card__price {
  font-size: 1.5rem;
  color: #222;
  font-weight: 500;
  margin-bottom: 1rem;
}

.card__link {
  text-decoration: none;
  padding: 1rem 1.6rem;
  color: #333;
  border-bottom: 2px solid #a0aec0;
  font-size: 125%;
  transition: all 0.3s ease-in-out;
}

.card__link:hover {
  background-color: #a0aec0;
  color: #fff;
}

@media only screen and (max-width: 768px) {
  .card h2 {
    font-size: 1.5rem;
  }
}

@media only screen and (max-width: 600px) {
  .card h2 {
    font-size: 1.2rem;
    padding: 1rem 0 0 1.25rem;
  }

  .card__details {
    padding: 0 1.25rem 1rem;
  }

  .card__detail {
    font-size: 1.05rem;
  }

  .card__price {
    font-size: 1.3rem;
  }

  .card__link {
    padding: 0.4rem 0.8rem;
    font-size: 100%;
    border-width: 1px;
  }

  .card__link span {
    display: none;
  }
}
</style>
