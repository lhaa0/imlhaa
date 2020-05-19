<template>
  <div class="home">
    <HelloWorld/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import { isMobileOnly } from 'mobile-device-detect'
import Vue from 'vue'

export default {
  name: 'Home',
  components: { HelloWorld }
} 

</script>
<style scoped lang="scss">
.home {
  width: 100%;
}
</style>