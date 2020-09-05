<template>
  <div id="app" @mousemove="ubicacion" class="container">
    <!-- <img
      :style="{left: x, top: y, position: 'absolute', width: '100px'}"
      src="https://media.giphy.com/media/2kTO2z0emYWekZ3MHf/giphy.gif"
      alt
    />-->
    <div id="nav" class="row justify-content-end">
      <router-link to="/">Home</router-link>
      <router-link to="/filtrados">Filtrados</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  data() {
    return {
      x: "20px",
      y: "10px",
    };
  },
  methods: {
    ubicacion(event) {
      this.x = event.clientX + "px";
      this.y = event.clientY + "px";
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: rgb(128, 64, 0);
  background: linear-gradient(
    138deg,
    rgba(128, 64, 0, 1) 43%,
    rgba(255, 255, 255, 1) 100%
  );
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
