<template>

  <div class="container">

    <div v-for="movie in movies" :key="movie.id" class="movies">
      
        <img :src="movie.avatar" alt="movies_in_theaters" class="capa">
       
        <p>{{movie.titulo}}</p>

    </div>

  </div>

</template>

<script>

import axios from 'axios';


export default {
  name: 'HomePage',
  data() {
    return {
         movies: [],
         
    }
  
  },
  mounted() {
    axios
      .get('https://api.b7web.com.br/cinema/')
      .then(json => {
        this.movies = json.data
        })
  }
}

</script>

<style scoped lang="scss">

.container {
 
 display: grid;
 grid-template-columns: 1fr 1fr 1fr;
  
}

.movies {
  text-align: center;
  margin: 30px;

  p {
    margin-top: 15px;
    text-align: center;
  }
}

.capa {
  height: 200px;
  width: 150px;
}

</style>
