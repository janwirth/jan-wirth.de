<template lang='pug'>
  ul
    slot
</template>

<style lang='stylus'>
shrinking-list li
  display: inline-block
  margin-right: 1em

shrinking-list li
  font-size: 10px
  transition: .1s
  transition-delay: .5s

shrinking-list:hover li
  opacity: 0.9 !important
  font-size: 14px !important

for child in 0 .. 50
  shrinking-list li:nth-child({child})
    transition-delay: (.02 * child )s
    font-size: (14 - (0.2 * child))px
    opacity: 0.3 + (0.7 / 19 * child)

</style>
