<script>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
export default {
  methods: {
    isMobile() {
      if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true
      } else {
        return false
      }
    }
  }
}
</script>

<template>
  <div class="relative">
    <div v-if="!isMobile()"
      class="absolute top-0 bottom-0 mx-auto left-1/2 transform -translate-x-1/2 z-0 w-full md:w-[1200px] lg:w-[1600px] max-w-screen">
      <img src="../public/img/pcBg.svg" class="hidden lg:block w-full h-full object-cover" alt="Shapes">
      <RouterView />
      
    </div>
    <div v-else
      class="absolute top-0 bottom-0 mx-auto left-1/2 transform -translate-x-1/2 z-0 w-full md:w-[1200px] lg:w-[1600px] max-w-screen">
      <!-- Mobile View-->
      <img src="https://www.letsjive.io/images/marketing/home-shapes-full.svg"
        class="hidden lg:block w-full h-full object-cover" alt="Shapes">
      <RouterView />
    </div>
  </div>
</template>