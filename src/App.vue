<template>
  <div class="container">
    <nav>
      <Header class="header" />
      <router-link to="/">
        <button class="linked-item">Home</button>
      </router-link>
    </nav>
    <router-view />
    <footer>
      Copywrite &copy; 2022
    </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style>
  body {
    background-color: black;
    color: white;
  }

  .container {
    margin: 20px;
  }

  nav h1 {
    color: white;
  }

  nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-bottom: 10px;
  }

  .link-items {
    flex: 0.5;
  }

  .header {
    flex: 1;
  }

  footer {
    margin-top: 50px;
    text-align: center;
  }
</style>
