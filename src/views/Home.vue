<template>
  <div class="home">
    <div id="cont-1">
      <div>
        <HomeSlider />
        <!--<HomeNav id="home-av" />-->
      </div>
    </div>
    <div id="cont-2">
      <AboutCo id="about" />
    </div>
  </div>
</template>
<script>
import HomeSlider from '../components/HomeSlider.vue'
import AboutCo from '../components/AboutCo.vue'
export default {
  components: {
    AboutCo,
    HomeSlider
  }
}
</script>
<style scoped>
.home {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
#about {
  width: 100%;
}
</style>
