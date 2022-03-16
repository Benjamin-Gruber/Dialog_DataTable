<template>
  <div class="text-center">
    <v-dialog v-model="dialog" width="500">
      <template v-slot:activator="{ on }">
        <v-btn v-on="on" class="text mt-5 mb-8 warning">Rennen hinzufügen</v-btn>
      </template>
      <v-card>
        <v-card-title class="h3 grey lighten-3" primary-title>Rennen erstellen</v-card-title>
        <v-card-text>
          <v-form class="px-3 mt-4">
            <v-text-field label="Title" v-model="newName"></v-text-field>
          </v-form>
          <v-form class="px-3 mt-4">
            <v-text-field label="Currency" v-model="rennen.ort"></v-text-field>
          </v-form>
          <v-form class="px-3 mt-4">
            <v-text-field label="Language" v-model="rennen.ort"></v-text-field>
          </v-form>
          <v-card-actions>
            <v-btn class="btn warning mx-0 mt-3 text">Save</v-btn>
          </v-card-actions>
        </v-card-text>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
