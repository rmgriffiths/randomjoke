<template>
  <v-container mb-12>
    Joke of the day
    {{ joke.setup }}
    <br />
    {{ joke.delivery }}
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
    const path = '/joke/Any'
    this.$axios.get(path).then((res) => {
      this.joke = res.data
    })
  },
}
</script>
