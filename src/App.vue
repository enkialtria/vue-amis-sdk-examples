<template>
  <div id="app">
    <vue-amis-sdk
        id='editorName'
        theme='cxd'
        className='is-fixed'
        :preview='isPreview'
        :isMobile='isMobile'
        @onChange='onChange'
        :value='schema'
    />
  </div>
</template>
<script>
import VueAmisSdk from 'vue-amis-sdk'
import 'vue-amis-sdk/lib/vue-amis-sdk.css'

export default {
  name: 'App',
  data() {
    return {
      isPreview: false,
      isMobile: false,
      schema: {}
    }
  },
  components: {
    VueAmisSdk: window.VueAmisSdk
  },
  methods: {
    onChange(e) {
      console.log(e)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
