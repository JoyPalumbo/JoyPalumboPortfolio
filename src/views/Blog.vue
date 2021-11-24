<template>
  <div class="about">
    <h1>Joy's Dev.to Blog Posts</h1> 
     <v-spacer class="ma-3"></v-spacer>
     <h4>This blog was created when I started school.  As part of our schoolwork we were required to write a blog post every week.  This was to be done outside our 11 school day.
     Due to lack of time, I didn't put much effort into these blog posts.  
     
     I have decided to start blogging again, but this time as a way to study topics I find difficult.  I will study the topics enough that I can write a blog post about that topic.
     I may through in some fun topics here and there but I will mainly use the blog to force myself to study hard-to-understand topics. 
     </h4>
       <v-spacer class="ma-2"></v-spacer>
    <h4 >The blog posts are pretty old, back from when I was in school in 2019. 
      <br>
      But stay tuned, I will be adding new blog posts soon!
    </h4>
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
<v-btn  class="ma-2"
      outlined
      color="pink" :href="blog.canonical_url" target="_blank">
   Click here to read full article
</v-btn>
      <!-- <v-card-text >
      Click here to read full article: {{blog.canonical_url}}
    </v-card-text> -->
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

