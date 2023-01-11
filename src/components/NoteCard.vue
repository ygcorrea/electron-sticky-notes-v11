<template>
  <v-card class="mx-auto" max-width="344">
    <v-card-title>
      {{ title }}
    </v-card-title>
    <v-card-text>
      <p>{{ content }} </p>
    </v-card-text>
    <v-card-actions>
      <v-btn text color="teal accent-4" @click="deleteNote(i)">
        {{ buttonText }}
      </v-btn>
    </v-card-actions>

  </v-card>
</template>
<script>
export default {
  name: 'NoteCard',
  props: {
    title: String,
    content: String,
    buttonText: String,

  },
  data: () => ({
    reveal: false,
  }),
}
</script>
<style>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
</style>