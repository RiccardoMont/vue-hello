<script>
export default {
  name: 'App',
  data() {
    return {
      msg: 'Mustache',
      img: 'https://picsum.photos/600/300',
      color: '#000000'
    }
  },
  methods: {
    colorRandomizer(){

      let n = (Math.random() * 0xfffff * 1000000).toString(16);
  	  return '#' + n.slice(0, 6);

    },
    myFunc(){

      this.color = this.colorRandomizer();

    }


  }
}
</script>

<template>
  <div>
    <h1>{{ msg }}</h1>
    <img :src="img" alt="random_img">
    <br>
    <button @click="myFunc" :style="{background: color}">Change my color!</button>

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
