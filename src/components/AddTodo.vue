<template>
  <div id="addto">
    <form @submit="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Add Todo List">
      <input type="submit" value="Submit" class="btn">

    </form>
  </div>
</template>

<script>
// import {v4 as uuid} from 'uuid';

export default {
  name: "AddTodo",
  data (){
    return {
      title: ''
    }
  },
  methods: {
    addTodo(e) {
      e.preventDefault()
      const newTodo = {
        // id: uuid(),
        title: this.title, 
        completed: false
      }
      this.$emit('add-todo', newTodo)

      this.title = ' '
    }
  }

}
</script>

<style scoped>

  #addto {
    padding: 10px;
  }
  form {
    display: flex;
  }
  input[type="text"] {
    flex: 10;
    padding: 10px;
  }
  input[type="submit"] {
    flex: 2;
  }

</style>>

