<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div class="bg">
    <header>
    <div class="outsideWindow">
      <img alt="Vue logo" class="logo" src="@/assets/jpg/head.jpg" width="125" height="125" />
    </div>

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  </div>
  <RouterView />
</template>

<style scoped>
.bg{
  width: 100%;
  height: 100%;
  background: linear-gradient(-75deg, #715633, #2b2522);
  mask: url(@/assets/jpg/Q版设计);
  mask-repeat: no-repeat;
  mask-position: center center;
}
header {
  line-height: 1.5;
  max-height: 100vh;
}
.outsideWindow{
  border-radius: 50%;
}
.logo {
  display: block;
  object-fit: cover;
  border-radius: 50%;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
