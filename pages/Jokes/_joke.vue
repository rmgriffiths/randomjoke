<template>
  <v-container mb-12>
    {{ joke }}
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      joke: [],
    }
  },
  computed: {},
  created() {
    const jokesId = this.$route.params.joke
    const path = '/jokes/' + jokesId
    this.$axios.get(path).then((res) => {
      this.joke = res.data
    })
  },
  methods: {},
}
</script>
