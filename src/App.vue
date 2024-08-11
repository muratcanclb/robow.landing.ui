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
  <body>
    <div v-if="!isMobile()"
      class="bodyPc">
      <RouterView />

    </div>
    <div v-else
      class="bodyMb">
      <RouterView />
    </div>
  </body>
</template>

<style>
body,html{
  height: 100%;
  margin: 0%;
}
.bodyPc {
  background-image: url('/img/pcBg.svg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
}

.bodyMb {
  background-image: url('/img/mobileBg.svg');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: 100%;
}
</style>