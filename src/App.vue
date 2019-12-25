<template>
  <div id="app">
    <div class="main">
  
     <All/>
     <Expense/>
      
      <Details/>
    
    
  
    <router-view/>
    </div>
  </div>
</template>

<script>
import All from '@/components/All.vue';
 import Expense from '@/components/Expense.vue';
 import Details from '@/components/Details.vue';






export default {
  name: 'App',
  components: {
    All,
    Expense,
    
    Details
   
    
  }
}
</script>


<style >
.main{
width: 400px;
min-width: 320px;
height: 600px;
min-height:600px;
background-color: #ffff;
color: #FFF;
margin: 0 auto;
border: 2px solid #2c9c91;
border-radius: 5px;
margin-top:30px;
}


#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
