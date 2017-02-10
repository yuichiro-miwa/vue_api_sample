<template>
  <main class="mdl-layout__content">
    <div class="page-content">
      <search></search>
      <div class="feed">
        <card
          v-for="gif in gifs"
          :gif="gif">
        </card>
      <div>
    </div>
  </main>
</template>

<style>
  main {
    background-color: #f6f6f6;
    width: 100%;
    margin: 0 auto;
  }
  .page-content {
    display: flex;
    flex-direction: column;
  }
  .feed {
    width: 80%;
    margin: 0 auto;
  }
</style>

<script>
import Search from './Search'
import Card from './Card'
import { mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters(['gifs'])
  },
  components: {
    Search,
    Card
  }
}
</script>

