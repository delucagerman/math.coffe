<template>
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
</template>

<script>
export default {
  name: "CardRatio",
  props: ["mostrarPesoLiquido"],
  data() {
    return {
      gramos: "",
      mostrar: "",
    };
  },
};
</script>

<style scoped>
</style>