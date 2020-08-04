<template>
  <div id="app">
    <div class="overlay"></div>
      <Cards v-bind:letters="letters"/>
    
  </div>
</template>


<script>

import Cards from "./components/Cards"

export default {
  name: 'App',
  components:{
    Cards
  },
  data(){
    return{
      letters:[
        {
          id:1,
          title:"a"
        },
        {
          id:2,
          title:"b"
        },
        {
          id:3,
          title:"c"
        }
      ],
      newcar:0
    }
  },
  methods: {
        changeCard(){
            var num = Math.floor(Math.random()*this.letters.length)
            this.newcar = num
        }
    },
}

</script>

<style>

#app{
  background: url('./assets/wood-bg-min.jpg')
}

</style>
