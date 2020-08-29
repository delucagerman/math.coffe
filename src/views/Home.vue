<template>
  <div class="home">
    <h1 class="mb-5">Math.Coffee</h1>

    <div class="row align-items-center">
      <div class="input-group mb-3 col-sm-7">
        <input
          v-model="gramos"
          type="text"
          class="form-control shadow p-3 mb-5 bg-white rounded"
          placeholder="¿Cuantos gramos de café molido lleva tú receta?"
          aria-label="Recipient's username"
          aria-describedby="button-addon2"
        />
        <div>
          <div class="input-group-append">
            <button
              @click="mostrarPesoLiquido"
              class="btn btn-outline-secondary shadow rounded"
              type="button"
              id="button-addon2"
            >Descubre el peso liquido</button>
          </div>
        </div>
      </div>

      <div class="col-sm-5 row justify-content-center">
        <div class="card shadow p-3 mb-5 bg-white rounded" style="width: 18rem;">
          <img src class="card-img-top" alt />
          <div class="card-body">
            <h2 class="card-title">Ratio 1:2</h2>
            <div v-show="mostrar">
              <h2 class="card-text">{{Math.round((gramos * 2)*100)/100}}</h2>
              <h3>Es tu peso liquido</h3>
            </div>
            <a href="#" class="btn btn-primary">Mas info</a>
          </div>
        </div>

        <div class="card shadow p-3 mb-5 bg-white rounded" style="width: 18rem;">
          <img src class="card-img-top" alt />
          <div class="card-body">
            <h2 class="card-title">Ratio 1:1.8</h2>
            <div v-show="mostrar">
              <h2 class="card-text">{{Math.round((gramos * 1.8)*100)/100}}</h2>
              <h3>Es tu peso liquido</h3>
            </div>
            <a href="#" class="btn btn-primary">Mas info</a>
          </div>
        </div>

        <div class="card shadow p-3 mb-5 bg-white rounded" style="width: 18rem;">
          <img src class="card-img-top" alt />
          <div class="card-body">
            <h2 class="card-title">Ratio 1:1.5</h2>
            <div v-show="mostrar">
              <h2 class="card-text">{{Math.round((gramos * 1.5)*100)/100}}</h2>
              <h3>Es tu peso liquido</h3>
            </div>
            <a href="#" class="btn btn-primary">Mas info</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      gramos: "",
      mostrar: false,
    };
  },
  methods: {
    mostrarPesoLiquido() {
      this.mostrar = !this.mostrar;
    },
  },
};
</script>
