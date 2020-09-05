<template>
  <div class="home">
    <h1 class="mb-5">Math.Coffee</h1>
    <transition appear name="filtro">
      <img class="filtro" src="@/assets/filtro.png" alt="filtro" />
    </transition>

    <div class="row align-items-center">
      <div class="input-group mb-3 col-sm-7">
        <input
          v-model="gramos"
          type="text"
          class="form-control shadow p-3 mb-5 bg-white rounded"
          placeholder="¿Cuantos gramos de café molido lleva tú receta?"
        />
        <div>
          <div class="input-group-append">
            <button
              v-if="!mostrar"
              @click="mostrarPesoLiquido"
              :disabled="mostrar == true"
              class="btn btn-secondary shadow rounded"
              type="button"
              id="button-addon2"
            >Descubre el peso liquido</button>
            <button
              v-else
              @click="reset"
              class="btn btn-secondary shadow rounded"
              type="button"
              id="button-addon2"
            >Reset</button>
          </div>
        </div>
        <p>El café espresso es una bebida realizada en una máquina de café, con una presión específica (9 bares) y a una temperatura específica (90/92 grados) en un tiempo determinado, en un rango de 20 a 30 segundos. Dicha bebida es saturada por la proporción de café utilizada en el porta filtro y el tiempo de extracción,pero bien preparada debe darnos como resultado una bebida equilibrada en cuerpo,corazón y crema además de resaltar su aroma en taza como así también poder percibir de la mejor manera sus atributos sensoriales en el paladar al momento de consumirla y luego en el post gusto.</p>
      </div>

      <div class="col-sm-5 row justify-content-center">
        <div
          v-for="(ratio, index) in ratios"
          :key="index"
          class="card shadow p-3 mb-5 bg-dark text-white rounded"
          style="width: 18rem;"
        >
          <img src="@/assets/2615.png" class="card-img-top animate__animated animate__flip" alt />
          <div class="card-body">
            <h2 class="card-title">Ratio 1:{{ ratio }}</h2>
            <div v-show="mostrar">
              <h3>Tu peso liquido es:</h3>
              <h3>{{Math.round((gramos * ratio)*100)/100}}g</h3>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",

  data() {
    return {
      gramos: null,
      mostrar: false,
      ratios: [2, 1.8, 1.5],
    };
  },
  methods: {
    mostrarPesoLiquido() {
      this.mostrar = !this.mostrar;
    },
    reset() {
      this.mostrar = false;
      this.gramos = null;
    },
  },
};
</script>
