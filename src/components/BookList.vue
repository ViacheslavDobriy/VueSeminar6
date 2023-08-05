<template>
  <BookVue v-for="book in books" :key="book.id" :book="book"/>
</template>

<script>
import BookVue from './Book.vue'

export default {
    name: 'BookList',
    components: {
        BookVue
    },
    data() {
        return {
            books: [
                {
                    name: 'Little Bird',
                    author: 'S. Jeans',
                    year: 2018,
                    details: 'Book about little bird',
                },
                {
                    name: 'The Witcher',
                    author: 'A. Sapkovskiy',
                    year: 2010,
                    details: 'Book about the witcher Geralt',
                },
                {
                    name: 'Choice',
                    author: 'Eva Eger',
                    year: 2001,
                    details: 'Book about choice',
                },
                {
                    name: 'Atomic Habbits',
                    author: 'James Clear',
                    year: 2020,
                    details: 'Book about atomic habbits',
                },
                {
                    name: 'Easy Order',
                    author: 'A. Vasilev',
                    year: 2022,
                    details: 'Book about easy order'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
</style>