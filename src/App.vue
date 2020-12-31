<template>
  <Hello msg="Welcome to Hello App"/>
  <Todos />
</template>

<script>
import Hello from './components/Hello.vue'
import Todos from './components/Todos.vue'

export default {
  name: 'App',
  components: {
    Hello,
    Todos,
  },
  data(){
    return{
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false
        },
        {
          id: 2,
          title: "Todo Two",
          completed: true
        },
        {
          id: 3, 
          title: "Todo Three",
          completed: false
        }
      ]
    } 
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
  .btn {
    display: inline-block;
    border: none;
    background: #555;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }
  .btn:hover {
    background: #666;
  }
</style>
