<template>
  <v-app>
     
    <v-app-bar app color="#CE93D8" dark>
      <v-layout justify-center wrap>
      <!-- <h4 class="ml-1">Joy Palumbo</h4> -->
      <!-- <v-spacer></v-spacer> -->

      <v-btn
        v-for="link in links"
        :key="`${link.label}-header-link`"
         large
  small
  text
   class="pt-1"
        rounded
        :to="link.url"
      >
        {{ link.label }}
      </v-btn>
        </v-layout> 
    </v-app-bar>
 
    <v-content>
      <spacer class="ma-1"></spacer>
      <router-view></router-view>
      <spacer class="ma-1"></spacer>
    </v-content>
    <v-footer color="#CE93D8" padless>
      <v-layout justify-center wrap>
        <!-- <v-icon>mdi-facebook</v-icon>
        <v-icon>mdi-twitter</v-icon>
        <v-icon>email</v-icon> -->

        <!-- <v-spacer pr-1></v-spacer> -->
        <!-- <i class="fab fa-facebook-square"></i> -->
        <v-btn
          v-for="link in links"
          :key="`${link.label}-footer-link`"
          color="white"
          text
          rounded
        class="my-2"
          :to="link.url"
        >
          {{ link.label }}
        </v-btn>
        <v-flex blue-grey darken-2 grey py-4 text-center grey--text xs12>
          <!-- {{ new Date().getFullYear() }} -->
          <h5 class="font-weight-thin">
            — Copyright © 2020 Joy Palumbo
          </h5>
          <!-- <v-icon>mdi-email</v-icon> -->
          <!-- <i class="material-icons">face</i> -->
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
import { mdiAccount } from "@mdi/js";
import axios from 'axios';
export default {
  name: "App",
  data() {
    return {
      data: {},
      username: 'joypalumbo',
      svgPath: mdiAccount,
      links: [
        {
          label: "Home",
          url: "/",
        },

        {
          label: "Portfolio",
          url: "/portfolio",
        },
        {
          label: "Resume",
          url: "/resume",
        },
        {
          label: "Contact",
          url: "/contact",
        },
                {
          label: "Blog",
          url: "/blog",
          props: true
        }
      ],
    };
  },
  mounted(){
  axios.get(`https://dev.to/api/articles?username=${this.username}`)
    .then(res => {
      this.data = res.data
      console.log("data", res.data)
      this.$router.push({name: "Blog", params: {data: this.data}})
    })
    .catch(err => {
      console.log(err)
    })
    // .finally(() => )
  }
  
  // methods: {
  //   getData(){

  //   let data = this
  //   // axios.get(`https://dev.to/api/articles?username={$username}`)
  //   // try {
  //    const response =  axios.get('https://dev.to/api/articles?username=joypalumbo')
  //    console.log("data", response.data.description)
  //    this.data = response.data
  //    console.log("data",data)
  //   }
  // }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  // background-color: #4dd0e1;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
