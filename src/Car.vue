<template>
<div>
  <h1>Name: {{carName}}/{{reverseName}}</h1>
  <h2>Year: {{carYear}}</h2>
  <button @click="changeCar">Change car</button>
  <button @click="changeFromAudi">Change from parent</button>
</div>
</template>

<script>
export default {
  props: {
    carName: {
      type: String,
      required: true
    },
    carYear: {
      type: Number
    },
    changeFromAudi: {
      type: Function
    }
  },
  methods:{
    changeCar() {
      this.carName = 'Reno',
       this.$emit('changeName', this.carName)
    }
  },
  computed: {
    reverseName(){
      return this.carName.split('').reverse().join('')
    }
  }
}
</script>

<style scoped>

</style>
