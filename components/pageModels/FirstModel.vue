<template>
  <div class="box purple">
    <div style="z-index: 3">
      <span class="jl_title"/><InputCursor/>
    </div>
    <div class="purple_mask"/>
    <div class="img_container">
      <img src="https://i.picsum.photos/id/254/1920/1080.jpg?hmac=QAkC8LdfZ0ylXKy5Z4-za1A7iock_D_cgjarL-SR9Nw" alt=""/>
    </div>
  </div>
</template>

<script>
import InputCursor from "../InputCursor";
import gsap from "gsap";

export default {
  components: {InputCursor},
  props:{

  },
  data(){
    return {
      height:12
    }
  },
  mounted() {
    gsap.to(".purple .jl_title",{
      duration: 6,
      text: {
        value: "Welcome to SC World",
      },
      delay: 1,
    });
  }
}
</script>

<style>
.purple{ background:#ae4efc }
.purple_mask{ z-index:2; background:#00000055; position:absolute; width:100%; height:100%; top:0;left:0; }
</style>
