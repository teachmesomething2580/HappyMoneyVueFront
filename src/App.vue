<template>
  <div id="app">
    <Advertisement />
    <Header />
    <router-view/>
    <Footer />
  </div>
</template>

<script>
import Advertisement from '@/components/common/Advertisement.vue'
import Header from '@/components/common/Header.vue'
import Footer from '@/components/common/Footer.vue'

import '@/assets/css/fonts/IcoMoon-Free.ttf'
import '@/assets/css/icon/IcoMoon.css'
import '@/assets/css/icon/icon.css'

export default {
  name: 'app',
  components: {
    Advertisement,
    Header,
    Footer
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

input:focus {
  outline: none;
}
</style>
