<template>

  <div class="black-bg" v-if="isModalWindowOpen == true">
    <div class="white-bg">
      <h4>Information</h4>
      <p>Contents</p>
      <button @click="isModalWindowOpen = false">close</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="(a, i) in menu" :key="i">{{ a }}</a>
  </div>  

  <!-- <div v-for="(a, i) in products" :key="i">
    <h4>{{ a }}</h4>
    <p>$5000</p>
  </div> -->


  <div v-for="(a, i) in rooms" :key="i">
    <img :src="rooms[i].image" class="room-img" alt="">
    <h4 @click="isModalWindowOpen = true">{{rooms[i].title}}</h4>
    <p>${{rooms[i].price}}</p>
    <button @click="reports[0] += 1" >Fake Deals</button> <span>reports : {{reports[0]}}</span>
  </div>

</template>

<script>

import data from './components/post.js';

export default {
  name: 'App',
  data(){
    return{
      rooms: data,
      isModalWindowOpen: false,
      reports: [0, 0, 0],
      menu: ["HOME", "Shop", "About"],
      products: ['SunnyBank', 'WestEnd', 'EastEnd']
      
    }
  },

  methods:{
    increase(){
      this.reports += 1;
    }
  },
  components: {
  }
}
</script>

<style>

body {
  margin: 0
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 20%;
  background: black;
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: wheat;
  border-radius: 8px;
  padding: 20px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue ;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
 
.menu p {
  color: rgb(40, 241, 13);
  font-size: 2.0rem;
}

.room-img{
  width: 100%;
  margin-top: 40px;
}

.bt1 {
  width: 80px;
  height: 35px;
  background: #2c3e50;
}
</style>
