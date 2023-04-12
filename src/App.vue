<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Welcome.vue'
</script>

<template>
  <header>
    <picture>
      <source srcset="@/assets/logo-dark.png" media="(prefers-color-scheme: dark)" >
      <img alt="Vue logo" class="logo" src="@/assets/logo.png" width="150" height="150" />
    </picture>

    <div class="wrapper">
      <Header msg="Hermeton-sur-Miel" />
      <nav>
        <RouterLink to="/">Accueil</RouterLink>
        <RouterLink to="/about">Acheter du miel</RouterLink>
      </nav>
    </div>
  </header>

 <RouterView class="routerView"/>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 1rem;
}


nav {
  width: 100%;
  font-size: 18px;
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
    margin: 0 1rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1.1rem;

    padding: 1rem 0;
    margin-top: 1rem;
    position: relative;
  }

}

</style>
