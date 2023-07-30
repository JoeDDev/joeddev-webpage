<template>
  <div class="user">
      <div class="prueba">
          <div class="first_name">
              <h1 class="heading">{{user_name}}</h1>
          </div>
          <div class="last_name">
              <h1 class="heading">{{last_name}}</h1>
          </div>
          <div class="user_alias">
              <h2 class="heading">@{{user}}</h2>
          </div>
          <div class="prueba">
            <div class="prueba">
                Hola mundo
            </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: "UserData",
    props: {

    },
    data(){
        return{
            user_name: "Jose David",
            last_name: "Rojas Fuentes",
            user: "joeddev"
        }
    }
}
</script>

<style scoped>
    .prueba{
        border-style: dotted;
    }
    .user{
        display: flex;
        font-family: 'Kanit', sans-serif;
        font-weight: bold;
        margin-left: 10%;
        margin-right: 10%;
    }
    .first_name{
        font-size: 70px;
        text-align: left;
        margin-top: 20%;
        padding-bottom: -10%;
    }
    .last_name{
        font-size: 35px;
        text-align: left;
        padding-top: 12px;
        padding: 0;
    }
    .user_alias{
        font-size: 30px;
        text-align: left;
        padding-top: 12px;
        padding: 0;
    }
    .heading{
        margin: 0;
    }
</style>