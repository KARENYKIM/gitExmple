<template>
  <div id="app">
   <img src="./assets/logo.png"> 
   <Login></Login>
   <router-view></router-view>
  </div>
</template>

<script>
import Login from './components/Login.vue'
import Join from './components/Join.vue'

export default {
  components:{
    'Login' : Login
  }


}
//   var router = [
//     {
//      path : '/join'
//     }
//  ];

//  var router = new VueRouter({
//    routes
//  });
  // var app = new vue({
  //   router
  // }).$mount('#app');
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>

