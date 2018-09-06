<template>
    <div id="app">
        <Bear/>
    </div>
</template>

<script>
import Bear from "./components/Bear";

export default {
    name: "App",
    components: {
        Bear
    }
};
</script>

<style>
    #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
    }
</style>
