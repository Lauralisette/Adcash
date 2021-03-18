<template>
  <div class="navbar">
    <router-link to="/">Home</router-link>
</div>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    
    <p>Kui soovid tagi lisada, siis vajuta 'space' või 'enter'!</p>
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};

</script>
<style>
p{
  color:white;
}
.navbar {
  overflow: hidden;
  background-color: #333;
  position: fixed;
  top: 0;
  width: 100%;
  height: 50px;
}

.navbar a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}
.home{
  margin-top: 30px;
}

</style>
