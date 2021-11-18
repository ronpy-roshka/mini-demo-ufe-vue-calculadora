<template >
  <div class="card">
    <div class="card-body">
      <div class="form-floating mb-3">
        <input
          type="number"
          class="form-control"
          id="number1"
          placeholder="Ingrese el primer numero a sumar"
          v-model="number1"
        />
        <label for="number1">Numero 1</label>
      </div>

      <div class="form-floating mb-3">
        <input
          type="number"
          class="form-control"
          id="number2"
          placeholder="Ingrese el segundo numero a sumar"
          v-model="number2"
        />
        <label for="number2">Numero 2</label>
      </div>

      <div class="form-floating input-group mb-3">
        <input
          style="padding-top: 15px !important"
          type="number"
          class="form-control"
          id="result"
          v-model="sumar"
          readonly
        /><span
          class="btn btn-success new-random input-group-text align-middle"
          style="display: inherit !important"
          id="newRandom"
          @click.prevent="newRandom"
          >New Random</span
        >
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      number1: 0,
      number2: 0,
    };
  },
  computed: {
    sumar() {
      return parseInt(this.number1) + parseInt(this.number2);
    },
  },
  mounted() {
    console.log(this.msg);
    this.newRandom();
  },
  methods: {
    newRandom() {
      this.number1 = parseInt(Math.random() * 100);
      this.number2 = parseInt(Math.random() * 100);
      //_ROOT_RANDOM_VALUE = parseInt(this.number1) + parseInt(this.number2);
      ImprimirRandom(parseInt(this.number1) + parseInt(this.number2));
    },
    saludar(nombre){
      console.log(`Hola ${nombre}`);
    }
  },
};
</script>
<style lang="scss">
.seccion-uno {
  background-color: #3faf7c;
  padding: 0.5rem;
}
.new-random {
  background-color: #d1e7dd !important;
  color: #0f5132 !important;
  border: 1px solid rgba(0, 0, 0, 0.125) !important;
}
</style>