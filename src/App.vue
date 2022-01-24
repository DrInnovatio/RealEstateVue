<template>
 <div class="menu">
    
    <h1>Aniss Real Estate</h1>

  </div>  

  <div class="black-bg" v-if="isModalWindowOpen == true">
    <div class="white-bg">
      <h4>Information</h4>
      <p>Detailed contents</p>
      <button class="bt" @click="isModalWindowOpen = false">Close</button>
    </div>
  </div>

 
  <div v-for="(a, i) in products" :key="i">
    <img class="room-img" src="./assets/room0.jpg"/>
    <h4 @click="isModalWindowOpen = true">{{rooms[0].title}}</h4>
    <p>{{rooms[0].price}}</p>
    <button @click="increasingNumber()">허위매물</button><span>call : {{call[i]}} </span>
  </div>

    <div class="menu">
    
    <a v-for="(tom, k) in items" :key="tom">{{k}}</a>

  </div>  
  <div v-for="(a, i) in products" :key="i">
    <img class="room-img" src="./assets/room1.jpg"/>
    <h4 @click="isModalWindowOpen = true">{{rooms[1].title}}</h4>
    <p>{{rooms[1].price}}</p>
    <button @click="increasingNumber()">허위매물</button><span>call : {{call[i]}} </span>
  </div>
  
    <div class="menu">
    
    <a v-for="(tom, k) in items" :key="tom">{{k}}</a>

  </div>  
  <div v-for="(a, i) in products" :key="i">
    <img class="room-img" src="./assets/room2.jpg"/>
    <h4 @click="isModalWindowOpen = true">{{rooms[2].title}}</h4>
    <p>{{rooms[2].price}}</p>
    <button @click="increasingNumber()">허위매물</button><span>call : {{call[i]}} </span>
  </div>

</template>

<script>

import data from './components/post.js';


export default {
  name: 'App',
  data(){
    return{
      rooms: data,
      closeModal: true,
      isModalWindowOpen: false,
      call: [0, 0, 0,],
      items: ['Home', 'Earl Estate', 'About'],
      products: ['SunnyBank', 'WestEnd', 'EastEnd'],
      cities: ['Sydney', 'New York', 'Tokyo'],
      cars: ["Hyundai", "Benz", "Toyota", "Honda", "Mazda"],
      price: [2000, 3200, 1900]
      
    }
  },

  methods:{
    increasingNumber(){
      this.call[0]
    }
  },
  components: {
  }
}
</script>

<style>
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


.menu p {
  color: rgb(40, 241, 13);
  font-size: 2.0rem;
}

.room-img{
  width: 10%;
  margin-top: 40px;
}

.black-bg {
  width:20%; 
  height: 30%;
  background: black;
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 80%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

.bt1 {
  width: 80px;
  height: 35px;
  background: #2c3e50;
}
</style>
