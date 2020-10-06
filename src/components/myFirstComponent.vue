<template>
<div class="hello">
    <h1>{{ title }}</h1>
    <button v-on:click="getAnswer">Yes or No ?</button>
    <p>
        {{ answer }}
    </p>
</div>
</template>

<script>
export default {
    name: "myFirstComponent",
    props: {},
    data() {
        return {
            title: "Decision Helper",
            options: ["yes", "no", "maybe"],
            answer: "Get your answer here",
        };
    },
    methods: {
        getAnswer: function () {
            var randomOptionIndex = Math.floor(Math.random() * this.options.length);
            this.answer = this.options[randomOptionIndex];
        },
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
}

a {
    color: #42b983;
}
</style>
