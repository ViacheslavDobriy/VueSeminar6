<template>
  <MovieListVue />
</template>

<script>
import BookListVue from './components/BookList.vue'
import MovieListVue from './components/MovieList.vue'

export default {
  name: 'App',
  components: {
    BookListVue,
    MovieListVue
  }
}
</script>

<style lang="scss">
</style>
