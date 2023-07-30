<template>
  <div class="user">
      <div class="">
          <div class="first_name">
              <h1 class="heading">{{user_name}}</h1>
          </div>
          <div class="last_name">
              <h1 class="heading">{{last_name}}</h1>
          </div>
          <div class="user_alias">
              <h2 class="heading">@{{user}}</h2>
          </div>
          <div class="sw-container ">
            <div class="data-sw-container">
                {{carrera}},{{country}}
            </div>
          </div>
          <div class="social-container">
              <div>
                  <img @click="show_telegram_qr" class="soc-sty" src="./img/social-logos/telegram.png" alt="">
                  <img class="soc-sty" src="./img/social-logos/twitter.png" alt="">
                  <img class="soc-sty" src="./img/social-logos/linkedin.png" alt="">
                  <img class="soc-sty" src="./img/social-logos/youtube.png" alt="">
                  <img class="soc-sty" src="./img/social-logos/instagram.png" alt="">
              </div>
          </div>
      </div>
      <div>
          <v-dialog
            v-model="telegram"
          >
               <v-card>
                    <v-card-text>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    </v-card-text>
                    <v-card-actions>
                    <v-btn color="primary" block @click="dialog = false">Close Dialog</v-btn>
                    </v-card-actions>
                </v-card>
          </v-dialog>
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
            user: "joeddev",
            carrera: "Software Engineer",
            country: "GUA",
            telegram: false,
        }
    },
    methods:{
        show_telegram_qr(){
            console.log("muesta qr")
            this.telegram = true
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
    .sw-container{
        padding-top: 20%;
        position: relative;
    }
    .data-sw-container{
        text-align: center;
        font-size: 150%;
        background-color: black;
        color: white;
        width: 100%;
        height: 40px;
        border-radius: 10px;
        padding-top: 3%;
        padding-bottom: 2%;
    }
    .social-container{
        text-align: left;
        width: 100%;
        height: 40px;
        border-radius: 10px;
        padding-top: 1%;
    }
    .soc-sty{
        width: 5%;
        height: 5%;
        padding-right:1%;
    }
    .soc-sty-x{
        width: 10%;
        height: 10%;  
    }
    @media screen and (max-width: 768px) {
        .user {
            flex-direction: column;
            align-items: center;
        }

        .first_name {
            font-size: 40px;
            text-align: center;
            margin-top: 10%;
        }

        .last_name,
        .user_alias {
            font-size: 25px;
            text-align: center;
            padding-top: 8px;
        }

        .sw-container {
            padding-top: 10%;
        }
    }
</style>