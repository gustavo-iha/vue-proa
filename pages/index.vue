<template>
  <main>
    <navbar />

    <button @click="toggleTitle">Tô bad hoje</button>

    <!-- <h1 v-show="showTitle">Hello world!</h1> -->

    <h1 v-if="showTitle">Hello world!</h1>
    <h1 v-else>Meh world!</h1>

    <p class="subtitle">Projeto novo que acabamos de criar, oia só! Rapidão hein.</p>

    <the-footer />
  </main>
</template>

<script>
import Navbar from '../components/Navbar.vue'
import TheFooter from './components/Footer.vue'

export default {
  name: 'Index',

  components: {
    TheFooter,
    Navbar
  },

  data () {
    return {
      showTitle: true,

      navegandoNoMapa: false,
      name: '...',
      imoveisFavoritos: []
    }
  },

  methods: {
    toggleTitle () {
      this.showTitle = !this.showTitle
    }
  }
}

</script>
