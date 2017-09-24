<template lang='pug'>
  #app
    canvas#canvas
    router-view
</template>

<script>
import background from './components/background'
background
export default {
  data () {
    if (global.window && (global.window.innerWidth > 1000)) {
      const c = window.document.querySelector('#canvas')
      console.log(c)
      background(c)
    }
    /* eslint-disable no-undef */
    /* eslint-enable no-undef */
    return {}
  }
}
</script>

<style lang='stylus'>
#canvas
  position: fixed
  top: 0
  left: 0
  min-height: 100vh
  min-width: 100vw
  @media print
    display: none

</style>
