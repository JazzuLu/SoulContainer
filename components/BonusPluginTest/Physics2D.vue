<template>

  <div class="feature" id="featureAnimation">
    <div id="featureBackground">
      <div class="dot" v-for="i in 80"></div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";

export default {
  props:{
    color:{type:String, default:"#fff"},
  },
  data(){
    return {
      morph : null
    }
  },
  mounted() {
    gsap.set('.dot', {
      backgroundColor: "random([#663399,#84d100,#cc9900,#0066cc,#993333])",
      scale: "random(0.4, 1)",
      x:400,
      y:340
    });
    // create the physics2D animation
    let tween = gsap.to('.dot', {
      duration: 2.5,
      physics2D: {
        velocity: "random(200, 650)",
        angle: "random(250, 290)",
        gravity: 500
      },
      delay: "random(0, 2.5)"
    });
  },
  methods:{
  }
}
</script>

<style scoped>
#featureAnimation {
  background-color: #000;
  height: 262px;
  overflow: hidden;
  position: relative;
  width: 800px;
  margin: auto;
}

.dot {
  position: absolute;
  background-color: #91e600;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  will-change: transform;
}
</style>
