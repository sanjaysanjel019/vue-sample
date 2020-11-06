<template>
  <div class="testvue">
    <span class="text-4xl capitalize font-semibold"> Popular Destinations</span>
    <div class="flex justify-center align-center flex-row">
    <Card :destinations="destinations" class="p-4 flex" >
      
    </Card>
    </div>
  </div>
</template>

<script>

import Card from './components/Card'

export default {
  name: 'App',
  components: {

    Card
  },
  data () {
    return {
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
