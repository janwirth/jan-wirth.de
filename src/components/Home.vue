<template lang='pug' scoped>
#home
  //  img(src='../assets/portrait.png' alt='portrait of Jan Wirth')#portrait
  #text-content
    section
      header
        span.job-title Software Engineer&emsp;-&emsp;
        a.link(href='mailto:contact@jan-wirth.de') contact@jan-wirth.de
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
            h3.testifier: a.link(target='_blank' href='https://immist.io') Immanuel Sterzik - immist.io
        li.entry
          .testimonal
            blockquote “Within a brief time frame and with great professionalism, Mr. Wirth developed a very good solution for the online presence of Boehle Consuling. I find it easy to recommend Mr. Wirth for a position in this field.”
            h3.testifier: a.link(target='_blank' href='https://boehle.consulting') Karl-Heinz Böhle - CEO Boehle Consulting

        li.entry
          .testimonal
            blockquote “We couldn't have done it without Jan, he is a software engineer I can recommend without any doubt.”
            h3.testifier: a.link(target='_blank' href='https://www.linkedin.com/in/mmelchger/') Michael Melchger - Engineer Raytheon Anschütz

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

<style lang='stylus' scoped>

// HOME
h1
  font-size: 72px
  line-height: 0
  height: 0
  margin-top: .5em
  margin-bottom: 1.3em
  letter-spacing: .025em

section:not(:first-child)
  margin-top: 50px

section:last-child
  margin-bottom: -100px

section
  position: relative

@media (min-width: 1000px)
  #home
    margin: 0 auto
    flex-grow: 0
    width: 360px
    padding: 200px 150px

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

header
  height: 30px
  line-height: 30px

.entry
  min-height: 40px
  
.company-logo
  transform: translateX(-17px)

for child in 1 .. 5
  section:nth-child({child})
    animation-delay: (.3 * (child - 1))s

@keyframes fade-in
  0%
    opacity: 0
    transform: translateY(20px)
  100%
    opacity: 1
    transform: translateY(0)

section
  animation: fade-in .5s ease-out
  animation-fill-mode: both

</style>
