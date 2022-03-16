<template>
  <div>
    <h2 class="mt-2 mb-2d">Browse all our books</h2>
    <v-data-table :headers="headers" :items="books" :items-per-page="10" class="elevation-1">
      <!-- eslint-disable-next-line -->
      <template v-slot:item.imageLink="{ item }">
        <v-img
          :src="item.imageLink"
          width="100"
          @click="
            dialog = true;
            selectedImg = item.imageLink;
          "
        ></v-img>
      </template>
      <!-- eslint-disable-next-line -->
      <template v-slot:item.actions="{ item }">
        <v-icon big class="mr-2 green--text"> mdi-pencil </v-icon>
        <v-icon big class="mr-2 red--text"> mdi-delete </v-icon>
      </template>
    </v-data-table>
    <v-dialog v-model="dialog" width="500"><BigPic :img="selectedImg" @close="dialog = false" /> </v-dialog>
  </div>
</template>

<script>
import BigPic from '@/components/BigPic.vue';
export default {
  name: 'Home',
  components: {
    BigPic,
  },
  props: {
    books: {
      type: Array,
    },
  },

  data() {
    return {
      selectedImg: '',
      dialog: false,
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
