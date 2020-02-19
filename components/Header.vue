<template>
  <header class="header">
    <ul class="nav-items">
      <li>
        <nuxt-link to="/" class="link">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/users" class="link">Users</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<style scoped>
  .header {
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: lightcoral;
  }

  .nav-items {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 80%;
  }

  .link {
    color: black;
    text-decoration: none;
  }
</style>