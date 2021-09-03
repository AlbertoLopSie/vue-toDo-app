<template>
  <div id="app">
    <div class="todo-wrapper">
      <div class="todo-container">
        <!-- <TodoList /> -->
        <todo-list :todos="todos" />
        <div class="todo-create-btn-container">
          <todo-create @formSubmitted="createTodo" />
        </div>
      </div>
    </div>
  </div>
</template>

<!-- JS part -->
<script>
import TodoList from '@/components/TodoList'
import TodoCreate from '@/components/TodoCreate'
export default {
  name: 'app',
  components: {
    TodoList, TodoCreate
  },
  data() {
    return {
      todos: [
        {
          _id: '1',
          title: 'Walk the dog',
          description: 'Go to forrest near the Zoo'
        },
        {
          _id: '2',
          title: 'Buy a bread',
          description: 'Whole grain bread would be good'
        },
        {
          _id: '3',
          title: 'Learn Programming',
          description: 'Preferable Tomorrow!'
        }
      ]
    }
  },
  // This function is run automaticaly by VUE framework
 
  methods: {
    createTodo(todo) {
      this.todos.push(todo)
    }
  }
}
</script>

<style> /*lang ="scss" agregar a style para usar scss;*/

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.app-form{
    color:slateblue;
  }
  label{
    display:block;
    font-size: 18px;
    font-weight: bold;
    padding: 5px;
  }
  .form-input{
    padding: 5px;
    font-size:17px;
    margin:5px;
    width: 300px;
  }

  .form-control{
    margin-bottom: 10px;
  }

.is-primary{
  background-color:rgb(59, 184, 59) !important ;
}
.app-button{
  font-size: 20px;
  padding: 10px;
  border-radius: 10px;
  background-color: #795899;
  color:white;
  font-weight: bold;  
 
  }
.app-button:hover{
  cursor:pointer;
}





.todo-create-btn-container{
  margin:10px; /* queda de 20px porque en el boton ya le habia agregado 10px */ 

}


.todo-wrapper {
  display:flex;
  justify-content: center;
  width: 100%;
}

.todo-container {
  display:flex;
  flex-direction: column;
  background-color:#d8d7d7;
  margin:0 auto;
  width:400px;
  min-height: 400px;
  border-radius: 10px;
}
.todo-list {
  background-color: rgb(235, 55, 55);
}


/** ASI QUEDARIA ESCRITO EN SCSS, 
.todo{
  
  &-wrapper {
    display:flex;
    justify-content: center;
    width:100%;
  }
  &-container {
    width:400px;
    min-height:400px;
    background-color:#ededed;
    border-radius:5px;
  }
  &-item{
    background-color:gray;
    min-height:70px;
    margin:10px;padding:10px;
    color:white;
    border-radius:5px;
    font-size:23px;

    7-contente{
      &-title{
        font-weight:bold;
      }
      &-description{
        font-size:19px;
      }
    }
  }
}
*/

</style>
