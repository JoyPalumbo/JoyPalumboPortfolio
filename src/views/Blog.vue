<template>
  <div class="about">
    <h1>Joy's Dev.to Blog Posts</h1> 
     <!-- <v-spacer></v-spacer> -->
    
    <ul class="blog">


     
  <li v-for="blog in posts" :key="blog.id">
  
     <v-card elevation="2" class="mx-auto ma-3"
    max-width="415">
    <div v-if="blog.cover_image !== null">
     <img :src="blog.cover_image" height="160px" class="ma-3"/>
     </div>
     <div v-else></div>

      <v-card-title class="justify-center">
        {{ blog.title }}
    </v-card-title>
    <v-card-subtitle class="text-center">
    {{blog.description}}
    </v-card-subtitle>

      <v-card-text >
      Click here to read full article: {{blog.canonical_url}}
    </v-card-text>
    </v-card>
  </li>
 
</ul>
  </div>
</template>

<script>
export default {
  name: "Blog",
  components: {},
  data () {
    return {

      posts: [],
    }
  },
  created(){
    this.posts=this.$route.params.data
    console.log('hello',this.$route.params.data)
  }

  
};
</script>

