<script>
export default {
  name: 'App',
  data() {
    return {
      msg: 'Mustache',
      img: 'https://picsum.photos/600/300'
    }
  },
  methods: {
    myFunc(){

      console.log('mi hai cliccato!')

    }
  }
}
</script>

<template>
  <div>
    <h1>{{ msg }}</h1>
    <img :src="img" alt="random_img">
    <br>
    <button @click="myFunc">Change my color!</button>

  </div>
  
</template>

<style>
h1{
  text-align: center;
  font-weight: bold;
  background: -webkit-linear-gradient(#4ba74b, #bd1aef);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

</style>
