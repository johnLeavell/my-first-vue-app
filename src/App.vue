<template>
  <div id="app">
    <div class="incrementer">
    <p>{{countString}}</p>
    <button @click="increment(10)">Increment!</button>
    </div>
  </div>
</template>



<script>
  export default {
      data() {
        return {
          count: 1
        }
    },
    computed: {
      countString(){
        return `The count is ${this.count}`
      }
    },
    methods: {
      increment(amount){
        this.count = this.count + amount
      }
    },
}
</script>




<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
