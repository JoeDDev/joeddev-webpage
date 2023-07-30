<template>
  <div class="container">
    <div class="left-side">

    </div>
    <div class="right-side">
      Hola mundo
      <img src="./img/usr_joeddev.jpg" alt="usr_img">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  display: flex;
  height: 100vh;
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
</style>
