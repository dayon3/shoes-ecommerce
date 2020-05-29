<template>
  <div class="navbar">
    <input type="checkbox" name="toggle" id="navbar-toggle" />
    <div class="logo"><a href="#home">K1CKS</a></div>

    <button
      class="hamburger hamburger--elastic navbar-btn"
      type="button"
      aria-label="Menu"
      aria-controls="navigation"
      @click="toggleClass"
    >
      <span class="hamburger-box">
        <span class="hamburger-inner"></span>
      </span>
    </button>

    <!-- <div class="navbar-btn">
      <label for="navbar-toggle">
        <span></span>
        <span></span>
        <span></span>
      </label>
    </div> -->

    <nav class="navbar-links" id="navigation">
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contacts">Contacts</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  methods: {
    toggleClass: () => {
      // Look for .hamburger
      const hamburger = document.querySelector('.hamburger')
      // On click
      hamburger.classList.toggle('is-active')
    }
  }
}
</script>

<style scoped>
.navbar {
  height: 6rem;
  width: 100%;
  background-color: #a0aec0;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
}

.navbar > .logo {
  display: inline;
  font-weight: bolder;
  padding: 1rem;
}

.navbar > .logo > a {
  font-size: 2.2rem;
  color: #fff;
  padding: 1rem;
  text-decoration: none;
}

.navbar > .navbar-btn {
  display: none;
}

.navbar > .navbar-links > ul {
  display: flex;
  font-size: 1.8rem;
  list-style: none;
  padding: 1rem;
}

.navbar > .navbar-links > ul > li > a {
  display: inline-block;
  padding: 1.3rem 1rem;
  text-decoration: none;
  color: #efefef;
}

.navbar > .navbar-links > ul > li > a:hover {
  background: rgba(0, 0, 0, 0.3);
}

.navbar > #navbar-toggle {
  display: none;
}

@media (max-width: 600px) {
  .navbar > .navbar-btn {
    display: block;
    position: absolute;
    right: 0;
    top: 0;
  }

  .hamburger {
    padding: 15px 15px;
    display: inline-block;
    cursor: pointer;
    transition-property: opacity, filter;
    transition-duration: 0.15s;
    transition-timing-function: linear;
    font: inherit;
    color: inherit;
    text-transform: none;
    background-color: transparent;
    border: 0;
    margin: 0;
    overflow: visible;
  }
  .hamburger:hover {
    opacity: 0.7;
  }
  .hamburger:focus {
    outline: none;
  }
  .hamburger.is-active:hover {
    opacity: 0.7;
  }
  .hamburger.is-active .hamburger-inner,
  .hamburger.is-active .hamburger-inner::before,
  .hamburger.is-active .hamburger-inner::after {
    background-color: #fff;
  }

  .hamburger-box {
    width: 40px;
    height: 24px;
    display: inline-block;
    position: relative;
  }

  .hamburger-inner {
    display: block;
    top: 50%;
    margin-top: -2px;
  }
  .hamburger-inner,
  .hamburger-inner::before,
  .hamburger-inner::after {
    width: 40px;
    height: 4px;
    background-color: #fff;
    border-radius: 4px;
    position: absolute;
    transition-property: transform;
    transition-duration: 0.15s;
    transition-timing-function: ease;
  }
  .hamburger-inner::before,
  .hamburger-inner::after {
    content: '';
    display: block;
  }
  .hamburger-inner::before {
    top: -10px;
  }
  .hamburger-inner::after {
    bottom: -10px;
  }

  .hamburger--elastic .hamburger-inner {
    top: 2px;
    transition-duration: 0.275s;
    transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
  }
  .hamburger--elastic .hamburger-inner::before {
    top: 10px;
    transition: opacity 0.125s 0.275s ease;
  }
  .hamburger--elastic .hamburger-inner::after {
    top: 20px;
    transition: transform 0.275s cubic-bezier(0.68, -0.55, 0.265, 1.55);
  }

  .hamburger--elastic.is-active .hamburger-inner {
    transform: translate3d(0, 10px, 0) rotate(135deg);
    transition-delay: 0.075s;
  }
  .hamburger--elastic.is-active .hamburger-inner::before {
    transition-delay: 0s;
    opacity: 0;
  }
  .hamburger--elastic.is-active .hamburger-inner::after {
    transform: translate3d(0, -20px, 0) rotate(-270deg);
    transition-delay: 0.075s;
  }

  /* .navbar > .navbar-btn > label {
    align-items: center;
    justify-content: center;
    display: inline-flex;
    flex-direction: column;
    width: 6rem;
    height: 6rem;
    padding: 1.3rem;
  }

  .navbar > .navbar-btn > label:hover,
  .navbar > #navbar-toggle:checked ~ .navbar-btn > label {
    background: rgba(0, 0, 0, 0.3);
  }

  .navbar > .navbar-btn > label > span {
    display: block;
    width: 3rem;
    height: 1rem;
    border-top: 2px solid #eee;
  } */

  .navbar > .navbar-links {
    position: absolute;
    display: block;
    width: 20rem;
    background-color: #333;
    transition: all 0.3s ease-in;
    overflow-y: hidden;
    top: 50px;
    right: 0;
  }

  .navbar > .navbar-links > ul {
    flex-direction: column;
    align-items: flex-end;
  }

  .navbar > .navbar-links > ul > li > a {
    display: block;
    width: 100%;
  }

  .navbar > #navbar-toggle:not(:checked) ~ .navbar-links {
    height: 0px;
  }

  .navbar > #navbar-toggle:checked ~ .navbar-links {
    height: max-content;
    overflow-y: auto;
  }
}
</style>
