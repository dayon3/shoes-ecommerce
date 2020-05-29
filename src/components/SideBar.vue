<template>
  <div class="sidebar">
    <aside>
      <ul>
        <li><a href="#">Men</a></li>
        <li><a href="#">Women</a></li>
        <li><a href="#">Kids</a></li>
        <li><a href="#">Nike</a></li>
        <li><a href="#">Adidas</a></li>
        <li><a href="#">Supreme</a></li>
        <li><a href="#">Off-White</a></li>
        <li><a href="#">Louis Vuitton</a></li>
        <li><a href="#">Vans</a></li>
        <li><a href="#">Converse</a></li>
        <li><a href="#">Adidas</a></li>
        <li><a href="#">Supreme</a></li>
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  name: 'SideBar'
}
</script>

<style scoped>
aside {
  width: 20vw;
}

ul {
  background: #a0aec0;
  border-radius: 0.3rem;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);
  list-style-type: none;
  padding: 2rem;
  margin-right: 2.5rem;
}

ul > li {
  padding: 0.5rem 0.25rem;
}

ul > li a {
  color: inherit;
  font-size: 1.8rem;
  text-decoration: none;
}

@media only screen and (max-width: 600px) {
  aside {
    display: none;
  }
}
</style>
