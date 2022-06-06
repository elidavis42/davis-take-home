<template>
  <NavBar/>
  <div style="height:100vh;width:100%" class="d-flex justify-content-center align-items-center">
    <FactDisplay :fact="fact" @new-fact="fetchData" v-show="showFact"/>
    <FetchButton @click="fetchData" v-show="showButton"/>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import FetchButton from './components/FetchButton.vue'
import FactDisplay from './components/FactDisplay.vue'

const API_URL = `https://uselessfacts.jsph.pl/random.json?language=en`;

export default {
  name: 'App',
  components: {
    NavBar,
    FetchButton,
    FactDisplay
  },
  data: () => ({
    fact: null,
    showButton: true,
    showFact: false
  }),

  methods: {
    async fetchData() {
      try {
        const data = await (await fetch(API_URL)).json()
        this.fact = data.text
        this.changeDisplay()
      } catch {
        this.fact = "We had an issue getting your fact."
        this.changeDisplay()
      }
    },
    changeDisplay () {
      this.showButton = false
      this.showFact = true
    }
  },
}
</script>
