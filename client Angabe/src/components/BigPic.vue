<template>
  <div class="text-center">
    <v-card>
      <v-img :src="img"></v-img>
      <v-card-actions class="d-flex justify-center">
        <v-btn color="black" text @click="$emit('close')"> close </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  props: {
    img: {
      type: String,
    },
  },
};
</script>

<style lang="scss" scoped></style>
