<template>
  <v-app>
    <NavBar />
    <v-main>
      <v-container> <router-view :books="books" /></v-container>
    </v-main>
  </v-app>
</template>

<script>
import books from '@/assets/books.json';
import NavBar from '@/components/NavBar.vue';
export default {
  name: 'App',

  data: () => ({
    books: books,
  }),

  components: {
    NavBar,
  },
};
</script>
