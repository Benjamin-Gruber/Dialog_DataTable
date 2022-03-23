<template>
  <div>
    <v-app-bar color="teal white--text">
      <img src="../assets/books.png" width="50px" alt="Books" />
      <v-toolbar-title>Books 'n More</v-toolbar-title>
      <img src="../assets/books.png" width="50px" alt="Books" />
      
      <v-spacer></v-spacer>
      <v-btn to="/" active-class=" deep-orange accent-2" class="mr-3 teal lighten-2 white--text">Home</v-btn>
      <v-btn to="/about" active-class="deep-orange accent-2" class=" mr-3 teal lighten-2 white--text">About</v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
