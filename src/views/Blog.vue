<template>
  <div class="about">
    <h1>Blog</h1>
    <ul id="blog">


     
  <li v-for="blog in posts" :key="blog.id">
     <v-card elevation="2" class="mx-auto pa-1"
    max-width="380">
      <v-img
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      height="150px"
    ></v-img>
      <v-card-title>
        {{ blog.title }}
    </v-card-title>
    <v-card-subtitle>
    {{blog.description}}
    </v-card-subtitle>
      <v-card-subtitle>
      Click here to read full article: {{blog.canonical_url}}
    </v-card-subtitle>
    </v-card>
  </li>
 
</ul>
    <!-- <h1>{{posts}}</h1> -->
    <!-- <h4 v-for="blog of posts"
  :key="blog.id"
  :blog-title="blog.title"
  :blog-description="blog.description"
  :blog-link="blog.canonical_url"
></h4> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import axios from 'axios'
export default {
  name: "Blog",
  components: {},
  data () {
    return {
      // posts: [],
      posts: [],
      // username: 'joypalumbo'
    }
  },
  created(){
    this.posts=this.$route.params.data
    console.log('hello',this.$route.params.data)
  }
  // props: {

  // }
  // beforeMount(){
  //   this.getData();
  // },
  // methods: {
  //   getData(){

    
  //   console.log("this", this.info)
  //   let data = this
  //   // axios.get(`https://dev.to/api/articles?username={$username}`)
  //   // try {
  //    const response =  axios.get('https://dev.to/api/articles?username=joypalumbo')
  //    console.log("data", response.data.description)
  //    this.data = response.data
  //    console.log("data",data)
  //   }
    // }
    // catch (e){
    //   console.log(e)
    // }

    // .the(res => {
    //   console.log("hewwo?", res.data)
    //   this.info = res.data})
    // .catch(err => console.log(err))
  // }
  
};
</script>

<style>
#blog {
  text-align: center;
}
</style>