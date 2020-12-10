<template>
  <div class="testvue">
    <span class="text-4xl capitalize font-semibold"> Popular Destinations</span>
    <div class="flex justify-center align-center flex-row">
    <Card :destinations="destinations" class="p-4 flex" >
      
    </Card>
    
    </div>
    <h1>Helo Guys</h1>
    <!-- <p v-for="(info,index) in infos" :key="index"> The title of the post is: {{info[1]}}  </p> -->
    <div v-if="error">
      {{error}}
    </div>
    <p v-else v-for="info in infos" :key="info.id"> The title of the posts are:  {{info.title}}</p>
  </div> 
</template>

<script>

import Card from './components/Card'
const axios = require('axios');

export default {
  name: 'App',
  components: {

    Card
  },
  data () {
    return {
      infos:[],
       // eslint-disable-next-line no-unused-labels
    destinations:[
      {name:'Tilicho Lake',
       description:'A beautiful lake with thousanads of Lorem ',
       image:'https://www.himalayadarshantreks.com/wp-content/uploads/2018/08/Tilicho-Lake-Short-Trek-Tilicho-Lake-Trek-848x525.jpg'
      },

      {name:'Rani Pokhari',
       description:'A strem of beautiful pearl filled water droplets that lets you win. ',
       image:'https://www.nepalitimes.com/wp-content/uploads/2020/07/Building-back-Rani-Pokhari-better-NT-6.jpg'
      },

      {name:'Beautiful Pokhara',
       description:'A heaven beneath the mountains that spark joy each time you visit. ',
       image:'https://cdn.kimkim.com/files/a/content_articles/featured_photos/0a99949f58bc92145369e8363c64c33bfd85f819/big-68acc559aad8def0f326f4d62e8faf78.jpg'
      }
    ]
  }
  },
  async mounted () {
    try{
      const response = await axios.get('http://localhost:1337/posts');
      this.infos = response.data;
    }
    catch(error){
      this.error = error;
    }
  }
    
   
}
</script>

<style >
.testvue{
  display: grid;
  width: 100%;
  place-items: center;
  width:100%;
  margin-top:200px;
}
</style>
