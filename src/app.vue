<template>
    <div id="app">
        <router-view v-if="$route.path=='/login'"></router-view>
        <index v-else></index>
    </div>
</template>
<script>
    import index from "@/views/index";

    export default {
        name: 'app',
        components: {
            index,
        },
        data() {
            return {}
        },
        mounted() {
            console.log(process.env.VUE_APP_BASE_URL)
        }
    }
</script>

<style>
    html, body {
        margin: 0;
        height: 100%;
    }

    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>