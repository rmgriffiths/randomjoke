<template>
  <v-container mb-12>
    <v-btn @click="display()">Try me</v-btn>
    <v-btn @click="display2()">Try me also</v-btn>
  </v-container>
</template>

<script>
export default {
  methods: {
    display() {
      window.open('jokes/Any')
    },
    display2() {
      this.$router.push('random')
    },
  },
}
</script>
