<template>
  <div>
    <h2>Add new one</h2>
    <input type="text" placeholder="name" v-model="name">
    <input type="text" placeholder="author" v-model="author">
    <input type="text" placeholder="year" v-model="year">
    <button @click="addMovie">Добавить новый фильм</button>
  </div>
</template>

<script>
export default {
    emits: ['addNewMovie'],
    name: 'MovieAdd',
    data() {
        return {
            name: '',
            author: '',
            year: ''
        }
    },
    methods: {
        addMovie() {
            const newMovie = {
                name: this.name,
                author: this.author,
                year: this.year
            };
            this.name = '';
            this.author = '',
            this.year = ''
            this.$emit('addNewMovie', newMovie);
        }
    },
}
</script>