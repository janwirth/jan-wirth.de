<template lang='pug'>
#home
  //  img(src='../assets/portrait.png' alt='portrait of Jan Wirth')#portrait
  #text-content
    section
      header
        span.job-title Software Engineer&emsp;-&emsp;
        a(href='mailto:contact@jan-wirth.de') contact@jan-wirth.de
      h1 Jan Wirth

    section
      h2 Skills
      ul
        li.entry 
          h3 Web Development
          points(v-bind:count='5')
        li.entry 
          h3 Project Management
          points(v-bind:count='2')
        li.entry 
          h3 Automation
          points(v-bind:count='2')
        li.entry 
          h3 Art & Design
          points(v-bind:count='3')
        li.entry 
          h3 Foreign Languages
          points(v-bind:count='3')
        li.entry 
          h3 Media
          points(v-bind:count='4')

    section
      h2 Experience
      ul
        li.entry
          a(target='_blank' href='https://cinteo.com').company-logo-wrap#cinteo-logo: img(src='../assets/cinteo-logo.png' alt='Cinteo company logo').company-logo
          points(v-bind:count='2')
        li.entry
          a(target='_blank' href='https://lesz.cool').company-logo-wrap#lesz-logo: img(src='../assets/lesz-logo.png' alt='Lesz company logo').company-logo
          points(v-bind:count='1')
        li.entry
          a(target='_blank' href='https://visual4.de').company-logo-wrap#visual4-logo: img(src='../assets/visual4-logo.png' alt='visual4 company logo').company-logo
          points(v-bind:count='3')

      footer.break-after: .print
        span.page-url jan-wirth.de
        span.page-number 1


    section
      h2 Testimonials
      ul
        li.entry
          .testimonal
            blockquote “Jan ist 1nicer boy.”
            h3.testifier Immanuel Sterzik - immist.io
        li.entry
          .testimonal
            blockquote “Within a brief time frame and with great professionalism, Mr. Wirth developed a very good solution for the online presence of Boehle Consuling. I find it easy to recommend Mr. Wirth for a position in this field.”
            h3.testifier Karl-Heinz Böhle - CEO Boehle Consulting

        li.entry
          .testimonal
            blockquote “We couldn't have done it without Jan, he is a software engineer I can recommend without any doubt.”
            h3.testifier Michael Melchger - Engineer Raytheon Anschütz

      footer: .print
        span.page-url jan-wirth.de
        span.page-number 2

//    section
//      h2 Education
//      ul
//        li.entry
//          a(target='_blank' href='https://hsg-eberbach.de').company-logo-wrap#dhbw-logo: img(src='../assets/hsg-logo.png' alt='Lesz company logo').company-logo
//        li.entry
//          a(target='_blank' href='https://dhbw-mosbach.de').company-logo-wrap#cinteo-logo: img(src='../assets/dhbw-logo.png' alt='Cinteo company logo').company-logo


</template>
<script>
import points from './Dots.vue'
export default {
  components: { points }
}
</script>

<style lang=stylus>

body
  margin: 0

h1
h2
  font-family: Montserrat, sans-serif;

h1
  font-size: 72px
  line-height: 0
  height: 0
  margin-top: .5em
  letter-spacing: .025em

h2
  font-size: 14px
  opacity: .5

h1
h2
h3
  font-weight: 400

section:not(:first-child)
  margin-top: 100px
section:last-child
  margin-bottom: -100px

section
  position: relative

#home
  font-family: Montserrat, sans-serif;
  position: relative
  background: white

@media (min-width: 1000px)
  #app
    display: flex
    justify-content: center

  #home
    margin: 0 auto
    flex-grow: 0
    width: 360px
    padding: 200px 150px
  body
    padding: 0 50px

@media screen and (max-width: 999px)
  body
    padding: 5vw

#portrait
  position: absolute
  top: 0
  left: 0
  width: 100px
  height: 139px

li
  list-style-type: none
.entry
  display: flex
  align-items: center

.entry h3
  transform: translateX(0)
  width: 150px
  font-family: Montserrat, sans-serif;
  font-size: 14px
  opacity: .8
  transition: .3s

.entry:hover h3
.entry:hover .company-logo
  opacity: 1

ul
  padding-left: 0

.company-logo
  transition: .3s
  height: 25px
  margin: 15px 0

.company-logo-wrap
  display: block
  width: 150px
  display: flex
  display: block
#lesz-logo
  transform: scale(.8) translateY(-2px) translateX(-5px)
#cinteo-logo
  transform: scale(.8)
#visual4-logo
  transform: scale(.55) translateX(-33px)

.entry .testifier
  font-style: italic
  display: block
  width: 100%


.testimonal
  margin-bottom: 20px

body
  max-width: 100vw
  overflow-x: hidden

header
  height: 30px
  line-height: 30px

.entry
  min-height: 40px
  
.company-logo
  transform: translateX(-17px)

blockquote
  margin: 0

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
  .page-url
    opacity: .3
    display: inline-block
    margin-right: 3em

blockquote
  line-height: 1.7

</style>
