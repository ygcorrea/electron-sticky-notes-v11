<template>
  <v-app>
    <v-main id="app">
      <div class="section__container">
        <h3>Sticky Notes</h3>
        <NoteCard title="my card title" content="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Laborum tempore ad, nemo rerum molestias eum unde similique voluptate saepe voluptas beatae fuga atque, exercitationem ipsa laudantium sed tempora. Architecto, optio!" buttonText="Deletar"/>
      </div>
    </v-main>
  </v-app>
</template>
   

<script>
import NoteCard from './components/NoteCard.vue'
export default {
  name: 'App',
  components: {

    NoteCard
  },
  data() {
    return {
      notes: [
        {
          id: 1, text: 'loremipsum',
        },
        {
          id: 2, text: 'loremipsum',
        }
      ]
    }
  },
  methods: {
    addNote() {
      this.notes.push({
        id: 3,
        text: 'loremipsum',
      })
    }
  }
}
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  margin: 0;
  background: #009578;
}

h3 {
  text-align: center;
}

</style>
