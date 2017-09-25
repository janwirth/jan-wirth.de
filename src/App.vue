<template lang='pug'>
  #app
    router-view
</template>

<style lang='stylus'>

// GLOBAL
body
  margin: 0
  user-select: none

h1
h2
h3
  font-family: Montserrat, sans-serif
  font-weight: 400

h2
  font-size: 14px
  opacity: .5
  position: relative
  text-transform: uppercase
  letter-spacing: 2px

h2:before
  opacity: .5
  position: absolute
  top: 10px
  left: -50px
  width: 35px
  height: 1px
  background: black
  display: block
  content: ''


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
    padding: 0 70px

@media screen and (max-width: 400px)
  body
    transform: scale(0.8) translateY(-10px) translateX(-20px)
@media screen and (max-width: 999px)
  body
    padding: 5vw

// PRINT
.print
  display: none

@media print
  .print
    display: block
  #experience
    margin-bottom: 3cm
  #recommendations
    margin-bottom: 8.1cm
  #Imprint
    margin-bottom: 2.6cm
#home
  width: 360px
  margin-left: auto
  margin-right: auto


.page-url
  opacity: .3
  display: inline-block
  margin-right: 3em
footer
  margin-top: 50px
  text-align: right
  width: 100%

a
  color: inherit
  text-decoration: none

.link
  display: inline-block
  position relative
  transition 0.3s
  padding: 0 5px // the trick
  margin: 0 -5px

.link:before
  content ''
  border-bottom 1px solid black
  position absolute
  bottom 2px
  left 0
  right 0
  margin 0 auto
  width 0
  transition 0.3s

.link:hover:before
  width 100%
  padding 0 // the other part of the trick
.link:active
  background black
  color white
  transition none

</style>
