<template>
    <v-container mb-12>
        Joke of the day
        <br />
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
        };
    },
    computed: {},
    created() {
        const jokesId = this.$route.params.joke;
        const path = "/joke/" + jokesId;
        this.$axios.get(path).then((res) => {
            this.joke = res.data;
        });
    },
    methods: {},
};
</script>
