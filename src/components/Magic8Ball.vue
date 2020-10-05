<template>
<div class="hello">
    <h1>{{ title }}</h1>
    <button v-on:click="getAnswer">Go</button>
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
            title: "Magic 8 Ball",
            options: [
                "As I see it, yes",
                "Ask again later",
                "Better not tell you now",
                "Cannot predict now",
                "Concentrate and ask again",
                "Don’t count on it",
                "It is certain",
                "It is decidedly so",
                "Most likely",
                "My reply is no",
                "My sources say no",
                "Outlook not so good",
                "Outlook good",
                "Reply hazy, try again",
                "Signs point to yes",
                "Very doubtful",
                "Without a doubt",
                "Yes",
                "Yes – definitely",
                "You may rely on it",
            ],
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
