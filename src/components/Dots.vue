<template lang='pug'>
.points
  .point(v-for='point in points') POINT
</template>

<script >
export default {
  props: ['count'],
  data () {
    return {
      points: this.count
    }
  }
}
</script>

<style lang='stylus'>
.points
  display: flex
  margin-left: 20px
.point
  opacity: .2
  margin: 10px
  color: transparent
  transition: .2s

  border-radius: 50%
  background: black
  print-color-adjust: exact; 
  width: 15px
  height: 15px


.entry:hover .point
  transform: scale3d(1.5, 1.5, 1.5)

for child in 1 .. 5
  .point:nth-child({child})
    transition-delay: (.02 * (child - 1))s

@media print
  body
    padding: 100px
  .point

    -webkit-print-color-adjust : exact
</style>
