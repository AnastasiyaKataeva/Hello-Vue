<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>My car name: {{ carName }}</h1>
    <app-car :car-name="carName" :car-year="carYear" @changeName="carName = $event" :change-from-audi="changeModel"></app-car>
  </div>
</template>

<script>
import Car from "./Car.vue";
export default {
  name: 'app',
  data () {
    return {
      carName: 'Mazda',
      carYear: '2009'
    }
  },
  methods: {
    changeModel(){
      this.carName = 'Audi'
    }
  },
 components: {
    appCar: Car,
 }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
