<template>
  <div>
    <div
      @click="isOpen = true"
      class="app-button">
      Create
    </div>
    <div class="modal" :class="{'is-active': isOpen}">
      <div class="modal-content">
        <span @click="close" class="close">&times;</span>
        <!-- <slot /> -->
      </div>
    </div>
  </div>
</template>
<script>
export default {
  // props: {
  //   close: {
  //     type: Boolean,
  //     required: false
  //   }
  // },
  data() {
    return {
      isOpen: false
    }
  },
  watch: {
    close(isClose /**,preIsCLose */) {
      if (isClose && this.isOpen) {
        this.isOpen = false
      }
    }
  },
  methods: {
    close() {
      this.isOpen = false
    }
  }
}
</script>

<style scoped>

  

  .close{
    color: #aaa;
    float: right;
    font-size:28px;
    font-weight: bold;
    line-height: 8px;
  }
  .close:hover{
    cursor: pointer;
  }
  .modal.is-active{
    display: block;
  }

  .modal{
    display:none;
    position:fixed; /*stay in place*/
    z-index:9999;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow:auto;  /* enable scrolling */
    background-color:rgba(0,0,0,0.4);
  }
  .modal-content{
    background-color:#fefefe;
    margin: 15% auto;
    padding:10px;
    border:1px solid #888;
    width:80%;
    text-align:left;
  }
</style>
