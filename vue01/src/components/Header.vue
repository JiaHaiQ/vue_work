<template>
    <header @click="changeTitle">
        <h1>{{title1}}{{title}}</h1>
    </header>
</template>

<script>
    export default {
        name: 'app-header',
        props:{
            title:{
                type:String
            }
        },
        data () {
            return {
                title1:"Vue.js Demo"
            }
        },
        methods:{
            changeTitle:function () {
                // this.title="changed"
                this.$emit("titleChanged","子向父组件传值")
            }
        }
    }
</script>

<style scoped>
    header{
        background: lawngreen;
        padding: 10px;
    }
    h1{
        color: #222;
        text-align: center;
    }
</style>
