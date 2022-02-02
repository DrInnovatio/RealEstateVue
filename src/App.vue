<template>
  <div class="menu">
    <a v-for="(a, i) in menu" :key="i">{{ a }}</a>
  </div>  

  <!-- <div v-for="(a, i) in products" :key="i">
    <h4>{{ a }}</h4>
    <p>$5000</p>
  </div> -->

  <div>
    <img src="./assets/room0.jpg" alt="">
    <h4>{{products[0]}}</h4>
    <p>$5,000</p>
    <button @click="reports[0] += 1" >Fake Deals</button> <span>reports : {{reports[0]}}</span>
  </div>

  <div>
    <h4>{{products[1]}}</h4>
    <p>$4,000</p>
    <button @click="reports[1] += 1"  >Fake Deals</button> <span>reports : {{reports[1]}}</span>
  </div>
  
  <div>
    <h4>{{products[2]}}</h4>
    <p>$7,000</p>
    <button @click="reports[2] += 1" >Fake Deals</button> <span>reports : {{reports[2]}}</span>
  </div>

 

</template>
 
<script>

//import data from './components/post.js';




export default {
  name: 'App',
  data(){
    return{
      // rooms: data,
      // closeModal: true,
      // isModalWindowOpen: false,
      // call: [0, 0, 0,],
      // items: ['Home', 'Earl Estate', 'About'],
      // products: ['SunnyBank', 'WestEnd', 'EastEnd'],
      // cities: ['Sydney', 'New York', 'Tokyo'],
      // cars: ["Hyundai", "Benz", "Toyota", "Honda", "Mazda"],
      // price: [2000, 3200, 1900]
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
