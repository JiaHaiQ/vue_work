<!--1模板：HTML结构-->
<template>
  <div id="app">
      <app-header @titleChanged="updateTitle($event)" v-bind:title="title"></app-header>
      <users v-bind:users="users"></users>
      <users v-bind:users="users"></users>
      <app-fooder v-bind:title="title"></app-fooder>
  </div>
</template>

<!--2行为：处理逻辑-->
<script>

//局部注册组件
import Users from './components/Users'
import Header from './components/Header'
import Fooder from './components/Fooder'


export default {
  name: 'App',
  data(){
    return{
      // title:"这是我的第一个vue-cli项目！"
        users:[
            {name:"九月",position:"卖月饼",show:false},
            {name:"八发",position:"卖豆腐",show:false},
            {name:"长江七号",position:"上天",show:false},
            {name:"赵六",position:"打工",show:false},
            {name:"王五",position:"销售",show:false},
            {name:"李四",position:"抓海鲜",show:false},
            {name:"三娘",position:"大小姐",show:false},
            {name:"二红",position:"唱戏",show:false},
            {name:"一佛",position:"军官",show:false},
        ],
        title:'传递的是一个值，（number string boolean）'
    }
  },
    methods:{
        updateTitle(title){
            this.title=title
        }
    },
    components:{
      // "users":Users,
        Users,
        "app-header":Header,
        "app-fooder":Fooder
    }
}
</script>
<!--3样式：解决样式-->
<style>
h1{
    color: purple;
}
</style>
