<template>
     <div>
          <div>
           <h3>Descubra o combústivel mais vantajoso! </h3>
            <label>
              Valor do Álcool
              <input
                type="number"
                min="1"
                max="200"
               v-model="alcool"
              />
            </label>

            <label>
              Valor gasolina
              <input
                type="number"
                min="1"
                max="200"
               v-model="gasolina"
              />
            </label>
          </div>
            <div>
            <p>
              <button class="waves-effect waves-light btn" @click="calc()">Calcular</button>
            </p>
          </div>
          </div>



</template>

<script>
export default {
  name: 'IGTI',
  data () {
    return {
      msg: 'IGTI',
      alcool: 0,
      gasolina: 0
    }
  },
  methods: {
    calc: function(){
    if (!this.alcool || !this.gasolina) {
      alert('Digite um valor para calcular');
      return;
    }

    let division = this.alcool / this.gasolina;

    if (division < 0.7) {
      alert('Abasteça com Álcool!')
    } else {
      alert('Abasteça com gasolina!')
    }


    }
  }
}
</script>

<style>

</style>
