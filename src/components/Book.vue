<template>
  <div class="book">
    <div class="book__content">
      <h1 class="book__name">{{ book.name }}</h1>
      <p class="book__author">{{ book.author }}</p>
      <p class="book__year">{{ book.year }}</p>
    </div>
    <div class="book__extra">
      <button class="book__button" @click="show">{{ !book.isShowed ? 'Показать доп информацию' : 'Скрыть доп информацию' }}</button>
      <p class="book__details" v-show="book.isShowed">{{ book.details }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Book',
  props: {
    book: Object
  },
  methods: {
    show() {
      if (this.book.isShowed) {
        this.book.isShowed = false;
      } else {
        this.book.isShowed = true;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
