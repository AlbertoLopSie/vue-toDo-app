


<template>
  
<div class="todo-item">
      <div class="todo-item-content">
        <div class="todo-item-content-title">
          {{title}}
        </div>
        <div class="todo-item-content-description">
         {{description}}
        </div>
      </div>
    </div>

</template>

<script>
export default {
  // props: ['title', 'description']
  props: {
    title: {
      type: String,
      required:true
    },
    description: {
       type: String,
       required: false,
       default: 'Default Description'
    },
    // en los props podes mandar Arrays, Objects, Strings, Number,Bolean, function
  }

  }


</script>



<style>
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
</style>