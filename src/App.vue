<template lang='pug'>
  #app
    router-view
</template>

<style lang='stylus'>

// GLOBAL
body
  margin: 0

h1
h2
h3
  font-family: Montserrat, sans-serif
  font-weight: 400

h2
  font-size: 14px
  opacity: .5

ul
  padding-left: 0

li
  list-style-type: none

blockquote
  margin: 0

// APP
body
  font-family: Montserrat, sans-serif;
  line-height: 1.7
  max-width: 100vw
  overflow-x: hidden

@media (min-width: 1000px)
  #app
    display: flex
    justify-content: center
  body
    padding: 0 50px

@media screen and (max-width: 999px)
  body
    padding: 5vw

// PRINT
.print
  display: none

@media print
  .print
    display: initial
  #home
    width: 360px
    margin-left: auto
    margin-right: auto
  footer
    margin-top: 50px
    text-align: right
  footer.break-after
    page-break-after: always
  footer.no-break
    page-break-after: avoid
  .page-url
    opacity: .3
    display: inline-block
    margin-right: 3em


</style>
