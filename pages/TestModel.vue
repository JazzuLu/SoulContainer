<template>
  <div class="container">
    <FirstModel/>
    <SecondModel/>
    <ThirdModel/>
    <FourthModel/>
    <FifthModel/>
  </div>
</template>

<script>
import FirstModel from "../components/pageModels/FirstModel";
import SecondModel from "../components/pageModels/SecondModel";
import ThirdModel from "../components/pageModels/ThirdModel";
import FourthModel from "../components/pageModels/FourthModel";
import FifthModel from "../components/pageModels/FifthModel";

export default {
  components:{
    FifthModel,
    FourthModel,
    ThirdModel,
    SecondModel,
    FirstModel,
  },
  mounted() {
    // console.log($)

  }
}
</script>
<style>
</style>
