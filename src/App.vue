<template>
  <div id="app" class="container">
    <div id="nav" class="row justify-content-end">
      <router-link to="/">Home</router-link>
      <router-link to="/filtrados">Filtrados</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #eee;
}

#nav {
  padding: 30px;
  background: rgb(207, 44, 44);
  background-image: url(https://images.unsplash.com/photo-1442411210769-b95c4632195e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60);
}

#nav a {
  font-size: 30px;
  font-weight: bold;
  color: #ffffff;
  text-shadow: 3px 3px 5px black;
  margin-right: 30px;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
