<template>
  <div>
    <v-data-table :headers="headers" :items="books" :items-per-page="10" class="elevation-1"></v-data-table>
  </div>
</template>

<script>
export default {
  name: 'Home',

  props: {
    books: {
      type: Array,
    },
  },

  data() {
    return {
      headers: [
        {
          text: 'Title',
          value: 'title',
        },
        { text: 'Image', value: 'imageLink' },
        { text: 'Country', value: 'country' },
        { text: 'Language', value: 'language' },
        { text: 'Actions', value: 'actions' },
      ],
      
    };
  },
};
</script>
