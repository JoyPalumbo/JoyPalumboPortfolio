<template>
  <div class="home">
    <div class="header">
      <div class="text-box">
        <h1 class="heading-primary">
          <span class="heading-primary-main"> Joy Palumbo</span>
          <span class="heading-primary-sub"> Software Engineer</span>
        </h1>
      </div>
    </div>
    <v-containter>
      <div class="about">
        <v-row>
          <v-col class="blue-grey--text text--darken-2">
            <spacer class="ma-2"></spacer>
            <h4 class="deep-purple--text text--lighten-3 pa-2">
              “Live as if you were to die tomorrow. Learn as if you were to live
              forever.” — Mahatma Gandhi
            </h4>
            <spacer class="ma-2"></spacer>
            <h1>About Me</h1>
            <spacer class="ma-1"></spacer>
            <v-card class="mx-auto" width="600px">
              <v-card-text>
                <!-- <h3 class="pa-md-4 mx-lg-auto" width="250px"> -->
                I am a fullstack Javascript developer who has a huge appetite
                for learning. I enjoy the diverse challenges that come with
                developing. Some of my favorite tools to use are ReactJS, VueJS
                , React Native and MySQL. When I'm not developing, I enjoy
                learning languages, such as Japanese and Korean, playing music,
                volunteering and crafting. Whether it's coding, or a hobby, I'm
                always learning something new!
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </div>
    </v-containter>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
};
</script>

<style scoped>
.header {
  height: 90vh;
  background-image: linear-gradient(
      to right bottom,
      hsla(300, 61%, 77%, 0.776),
      hsla(305, 74%, 63%, 0.776)
    ),
    url(../assets/mt.fuji.jpg);
  background-size: cover;
  background-position: top;
  position: relative;

  clip-path: polygon(0 0, 100% 0, 100% 75%, 0 100%);
}

.heading-primary {
  color: #fff;
  text-transform: uppercase;
}

.heading-primary-main {
  display: block;
  font-size: 50px;
  /* font-weight: 700; */
  letter-spacing: 18px;
  /* margin-bottom: 5px; */
}

.heading-primary-sub {
  display: block;
  font-size: 20px;
  margin-top: 5px;
  /* font-weight: 700; */
  letter-spacing: 18px;
}

.logo-box {
  position: absolute;
  top: 40px;
  left: 40px;
}

.text-box {
  position: absolute;
  top: 45%;
  left: 25%;
  transform: translate(-15%, -50%);
}



@media screen and (min-width: 601px) {
  .heading-primary-main {
    font-size: 80px;
    
  }
    .heading-primary-sub {
    font-size: 50px;
    /* margin-left */
  }
}

@media screen and (max-width: 600px) {
  .heading-primary-main {
    font-size: 30px;
   
  }
    .heading-primary-sub {
    font-size: 18px;
  }
  .text-box {
    left: 20%
  }
}
</style>
