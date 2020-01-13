<template>
  <div class="some-box">
    <label>
      The box
      <input type="text" v-model="boxVal">
    </label>
    <button @click="logBox">Submit</button>
    <ul class="places">
      <li :key="index" :title="key" v-for="(item, key, index) in names" v-text="item"/>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "SomeBox",
    methods: {
      logBox () {

        if (this.boxVal === 'Sinza') {
            this.names['hoes'] = this.boxVal;
        }

        if (this.boxVal === 'Gongo la Mboto') {
            this.names['huge buses'] = this.boxVal;
        }

        this.boxVal = ''
      }
    },
    data() {
      return {
        boxVal: '',
        names: {
            airport: 'Ukonga',
            goatSales: 'Vingunguti',
            barsEverywhere: 'Tabata',
            market: 'Buguruni'
        }
      }
    }
  }
</script>

<style scoped>
  * {
    font-size: large
  }
  button {
    margin: 1em;
    padding: .5em
  }
  ul {
    list-style-type: none
  }
</style>