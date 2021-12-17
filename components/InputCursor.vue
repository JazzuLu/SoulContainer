<template>

  <div class="input_cursor_container">
    <div class="input_cursor" :style="`backgroundColor:${color};width:${width}px;height:${height}px;`">&nbsp;</div>
  </div>
</template>

<script>
import $ from "jquery";

export default {
  props:{
    color:{type:String, default:"#fff"},
    width:{type:[String,Number], default:10},
  },
  data(){
    return {
      height:12
    }
  },
  mounted() {
    const $c =  $(`.input_cursor_container`);
    this.height = parseFloat($c.css('fontSize')) ?? 12;
  }
}
</script>

<style>
  .input_cursor_container{
    display:inline-block;
  }
  .input_cursor{
    display:flex;
    align-items:center;
    animation: bounce 1s infinite;
  }
  @keyframes bounce{
    from{ opacity:0 }
    to{ opacity:1 }
  }
</style>
