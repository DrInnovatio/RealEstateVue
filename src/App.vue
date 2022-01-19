<template>
  <div class="menu">
    
    <a v-for="(tom, k) in items" :key="tom">{{k}}</a>

  </div>  
  <div v-for="(a, i) in products" :key="i">
    <h4>{{a}}</h4>
    <p>$50</p>
  </div>
  

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      items: ['Home', 'Earl Estate', 'About'],
      products: ['SunnyBank', 'WestEnd', 'EastEnd'],
      cities: ['Sydney', 'New York', 'Tokyo'],
      cars: ["Hyundai", "Benz", "Toyota", "Honda", "Mazda"],
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
</style>
