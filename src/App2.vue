<template>
<div>
    <HeaderComponent />
    <myFirstComponent />
    <Magic8Ball />
</div>
</template>

<script>
import myFirstComponent from "./components/myFirstComponent.vue";
import Magic8Ball from "./components/Magic8Ball.vue";
import HeaderComponent from "./components/HeaderComponent.vue";

export default {
    name: "App",
    components: {
        myFirstComponent,
        Magic8Ball,
        HeaderComponent,
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
