<template>
 <div id="app">
    <div class="todo-wrapper">
      <div class="todo-container">
        <todo-list />
      </div>
    </div>
  </div>
</template>

<script>
import TodoList from '@/components/TodoList'
export default{
  name: 'app',
  components: {
    TodoList
  },
}
</script>

<style> /*lang ="scss" agregar a style para usar scss;*/

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.todo-wrapper {
  display:flex;
  justify-content: center;
  width: 100%;
}
.todo-container {
  background-color:#d8d7d7;
  margin:0 auto;
  width:400px;
  min-height: 400px;
  border-radius: 10px;
}
.todo-list {
  background-color: rgb(235, 55, 55);
}
.todo-item{
  background-color:slateblue;
  color:#fff;
  margin:10px;
  padding:10px;
  height:70px;
  border-radius:10px;
  font-size: 23px;
}
.todo-item-content-title{
  font-weight: bold;
}
.todo-item-content-description{
  font-size:19px;
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
