<template>
    <MovieInfoVue v-for="movie in movies" :key="movie.id" :movie="movie"/>
    <MovieAddVue @addNewMovie="addNewMovie"/>
  </template>
  
  <script>
  import MovieAddVue from './MovieAdd.vue'
  import MovieInfoVue from './MovieInfo.vue'

  export default {
      name: 'MovieList',
      components: {
        MovieInfoVue,
        MovieAddVue
      },
      data() {
          return {
            movies: [
                {
                    name: 'Ace Ventura 1',
                    author: 'Me',
                    year: 2001
                },
                {
                    name: 'Ace Ventura 2',
                    author: 'He',
                    year: 2002
                },
                {
                    name: 'Ace Ventura 3',
                    author: 'She',
                    year: 2003
                }
            ]
          }
      },
      methods: {
        addNewMovie(newdataMovie) {
            this.movies.push(newdataMovie);
        }
      },
  }
  </script>