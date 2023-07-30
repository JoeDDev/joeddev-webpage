<template>
  <div class="container">
    <div class="left-side">
      <DataUser/>
    </div>
    <div class="right-side">
      <img class="usr_img" src="./components/img/usr_joeddev.jpg" alt="usr_img">
    </div>
  </div>
</template>
 
<script>
import DataUser from './components/DataUser.vue'

export default {
  name: 'App',
  components: {
    DataUser
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
.container {
  display: flex;
  height: 100vh;
  margin: 0%;
}

.left-side,
.right-side {
  flex: 1;
  height: 100%;
}

.left-side {
  background-color: #ffffff; /* Color del lado izquierdo */
}

.right-side {
  background-color: #000000; /* Color del lado derecho */
}
.usr_img{
  max-width: 100%;
  max-height: 100%;
  object-fit: cover;
}
</style>
