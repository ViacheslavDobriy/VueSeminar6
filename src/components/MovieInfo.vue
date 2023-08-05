<template>
    <div class="movie">
        <h1 class="movie__name">{{ movie.name }}</h1>
        <p class="movie__author">{{ movie.author }}</p>
        <p class="movie__year">{{ movie.year }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'MovieInfo',
    props: {
      movie: Object
    }
  }
  </script>