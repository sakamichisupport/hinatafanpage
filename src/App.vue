<template>
  <h1>日向坂46応援サイト(仮)</h1>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/member">Member</router-link> |
    <router-link to="/discography">Discography</router-link> |
    <router-link to="/sns">SNS</router-link>
  </nav>
  <router-view/>
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
  color: #7cc7e8;
}
</style>
