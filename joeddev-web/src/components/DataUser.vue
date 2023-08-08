<template>
  <div class="user">
    <div>
      <div class="first_name">
        <h1 class="heading">{{ user_name }}</h1>
      </div>
      <div class="last_name desktop">
        <h1 class="heading">{{ last_name }}</h1>
      </div>
      <div class="user_alias">
        <h2 class="heading">@{{ user }}</h2>
      </div>
      <div class="sw-container">
        <div class="data-sw-container">
          {{ carrera }}{{ " " }}, {{ country }}
        </div>
      </div>
      <div class="social-container">
        <div>
          <a v-for="data in social_data" :key="data.name" :href="data.url" target="_blank">
            <img class="soc-sty" :src="require('@/assets/img/social-logos/' + data.img)" :alt="data.name">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UserData",
  props: {},
  data() {
    return {
      user_name: "Jose David",
      last_name: "Rojas Fuentes",
      user: "joeddev",
      user_image: "joeddev.jpg",
      carrera: "Software Engineer",
      country: "GUA",
      telegram: false,
      social_data: [
        {
          name: "telegram",
          img: "telegram.png",
          url: "https://t.me/JD_Rojas"
        },
        {
          name: "twitter",
          img: "twitter.png",
          url: "https://twitter.com/JoeDDev"
        },
        {
          name: "linkedin",
          img: "linkedin.png",
          url: "https://www.linkedin.com/in/joeddev/"
        },
        {
          name: "youtube",
          img: "youtube.png",
          url: "https://www.youtube.com/channel/UC74QGzPdzHHS7p6L0pVnPPw"
        },
        {
          name: "instagram",
          img: "instagram.png",
          url: "https://www.instagram.com/joeddev/"
        }
      ],
      isMobile: false
    };
  },
  mounted() {
    this.checkDevice();
    window.addEventListener("resize", this.checkDevice);
  },
  methods: {
    checkDevice() {
      this.isMobile = window.innerWidth <= 768;
    }
  },
  beforeUnmount() {
    window.removeEventListener("resize", this.checkDevice);
  }
};
</script>

<style scoped>
.user {
  display: flex;
  font-family: "Kanit", sans-serif;
  font-weight: bold;
  color: black;
  margin-left: 10%;
  margin-right: 10%;
}

.first_name {
  font-size: 70px;
  text-align: left;
  margin-top: 20%;
}

.last_name {
  font-size: 35px;
  text-align: left;
  padding-top: 12px;
}

.user_alias {
  font-size: 20px;
  text-align: left;
  padding-top: 12px;
}

.heading {
  margin: 0;
}

.sw-container {
  padding-top: 20%;
  position: relative;
}

.data-sw-container {
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

.social-container {
  margin-top: 5%;
  text-align: center;
  width: 100%;
  height: 40px;
  border-radius: 10px;
  padding-top: 1%;
}

.soc-sty {
  width: 5%;
  height: 5%;
  padding-right: 1%;
}

.soc-sty-x {
  width: 10%;
  height: 10%;
}

@media screen and (max-width: 768px) {
  .user {
    margin-top: 5%;
    margin-bottom: 5%;
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

  .desktop {
    display: none;
  }

  .soc-sty {
    width: 8%;
    height: 8%;
    padding-right: 2%;
  }
}

@media screen and (min-width: 769px) {
  .mobile {
    display: none;
  }
}
</style>
