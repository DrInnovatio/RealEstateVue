<template>
  <div class="menu">
    
    <a v-for="jojo in items" :key="jojo">{{jojo}}</a>
  </div>  
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h1>{{products[0]}} House</h1>
    <p>Price is {{price1}}</p>
  </div>
  <div>
    <h1>{{products[1]}} House</h1>
    <p>Price is {{price2}}</p>
  </div>
  <div>
    <h1>{{products[2]}} House</h1>
    <p>Price is {{price3}}</p>
  </div>
  

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      items: ['Home', 'Earl Estate', 'About'],
      products: ['SunnyBank', 'WestEnd', 'EastEnd'],
      price1: 2000,
      price2: 1200,
      price3: 3100
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
  margin-top: 60px;
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
</style>
