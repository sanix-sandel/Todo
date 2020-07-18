<template>
  <div id="app">
    <h4 class="bg-primary text-white text-center">
      {{name}}'s To Do List
    </h4>

    <div class="container-fluid p-4">
      <div class="row">
        <div class="col font-weight-bold">Task</div>
        <div class="col-2 font-wight-bold">Done</div>
      </div>
      <div class="row" v-for="t in tasks" v-bind:key="t.action">
        <div class="col" >{{t.action}}</div>
        <div class="col-2">{{t.done}}</div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      name:"Sanix",
      tasks:[
        {action:"Buy Flowers", done:false},
        {ation:"Get shoes", done:false},
        {action:"Collect tickets", done:true},
        {action:"Call Joe", done:false}
      ]
    }
  }
 
}
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
