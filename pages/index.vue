<template>
  <div class="container">
    <div class="middlebox">
      <h1>Vue-live test</h1>
      <vue-live
        :code="'<span>test</span> <Logo />'"
        :components="registeredComponents"
      />
    </div>
  </div>
</template>

<script>
import 'prismjs/themes/prism-tomorrow.css'
import { VueLive } from 'vue-live'
import Logo from '~/components/Logo'

export default {
  components: {
    VueLive
  },
  data() {
    return {
      registeredComponents: { Logo }
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.middlebox {
  width: 800px;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
