<template lang='pug' scoped>
#home
  //  img(src='../assets/portrait.png' alt='portrait of Jan Wirth')#portrait
  #text-content
    section#intro
      header
        span.job-title Software Engineer&emsp;-&emsp;
        a.link(href='mailto:contact@jan-wirth.de') contact@jan-wirth.de
      h1 Jan Wirth

    section#skills
      h2 Skills
        span(style='opacity: 0.5')  Touch for more
      ul
        li.skill
          .entry
            h3 Web Development
            points(v-bind:count='5')
          p.skill-text I have several years of experience developing web applications on a scale from tiny to huge.
            |  I worked alone or with local, distributed, national or international teams.
        li.skill
          .entry
            h3 Automation
            points(v-bind:count='4')
          p.skill-text Automation is key to efficiency and quality.
            |  A successfully automated task has direct positive impact on a enterprise's bottom line.
            |  Automation is of high priority in my work because it creates shared lasting value.
        li.skill
          .entry
            h3 Project Management
            points(v-bind:count='3')
          p.skill-text Good managament means assigning available resources to tasks that improve customer-value.
            |  I have experience in the management of technical projects, events and in my self-employed work.
        li.skill
          .entry
            h3 Design / Art /  UX
            points(v-bind:count='3')
          p.skill-text
            |  I have used Usability metrics to assess customer experience.
            |  Because of my background in Art and Design I understand the key value of design for a good product.
        li.skill
          .entry
            h3 Foreign Languages
            points(v-bind:count='3')
          p.skill-text
            |  My English is business fluent. Of French and Spanish I have basic but working knowledge.
        li.skill
          .entry
            h3 Media
            points(v-bind:count='4')
          p.skill-text I have solid experience with media processes for both print and digital.

    section#experience
      h2 Experience
        span(style='opacity: 0.5')  In years
      ul
        li.entry.enterprise
          a(target='_blank' href='https://cinteo.com').company-logo-wrap#cinteo-logo: img(src='../assets/cinteo-logo.png' alt='Cinteo company logo').company-logo
          p.skill-text
            |  Cinteo develops enterprise-grade web applications for Mercedes-Benz.
          points(v-bind:count='1')
        li.entry.enterprise
          a(target='_blank' href='https://lesz.cool').company-logo-wrap#lesz-logo: img(src='../assets/lesz-logo.png' alt='Lesz company logo').company-logo
          p.skill-text
            |  Lesz creates custom web sites and applications.
          points(v-bind:count='2')
        li.entry.enterprise
          a(target='_blank' href='https://visual4.de').company-logo-wrap#visual4-logo: img(src='../assets/visual4-logo.png' alt='visual4 company logo').company-logo
          p.skill-text
            |  visual4 designs, developes and distributes web sites, applications and CRM systems.
          points(v-bind:count='3')

    section#linkout
      h2 References
        span(style='opacity: 0.5')  And social media
      .references
        a.reference(target='_blank' href='https://codepen.io/franzskuffka'): img(src='../assets/codepen-logo.png')
        a.reference(target='_blank' href='https://github.com/franzskuffka'): img(src='../assets/github-logo.png')
        a.reference(target='_blank' href='https://linkedin.com/in/janwirth'): img(src='../assets/linkedin-logo.png')
        a.reference(target='_blank' href='https://xing.de/profile/Jan_Wirth6'): img(src='../assets/xing-logo.jpg')

    footer#footer-1.print
      span.page-url jan-wirth.de
      span.page-number 1
    div(style='page-break-after: always')


    section#recommendations
      h2 Recommendations
      ul
        //li.entry
        //  .testimonal
        //    blockquote “Jan is an extremely competent and reliable developer. He manages tasks in an efficient and reliable way, but does not hesitate in giving constructive feedback when a better solution could be achieved. He is a very professional colleague to work with.”
        //    h3.testifier: a.link(target='_blank' href='https://matchplan.de') Immanuel Sterzik - CTO Matchplan
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
    div(style='page-break-after: always')

    section#Tools
      h2 Tools / Methods
      p I have successfully used many different technologies and methods.
      shrinking-list
        li d3.js
        li React
        li Redux
        li Elm
        li MobX
        li AngularJS
        li VueJS
        li jQuery
        li WebPack
        li ES6
        li CoffeeScript
        li CSS
        li Stylus
        li Sass
        li Less
        li Pug
        li NodeJS
        li Data visualisation
        li E-Mail templating
        li TDD
        li BDD
        li Rapid prototyping
        li User Story Mapping
        li Requirements Analysis
        li Operation
        li Security
        li Machine Learning
        li Web Scraping
        li Functional Programming
        li Natural Language Processing
        li Sound Design
        li Reason
        li 3DS Max
        li Blender
        li Sketch
        li Adobe CC

    section#Education
      h2 Education / Awards
      ul
        li.entry.enterprise
          a(target='_blank' href='https://dhbw-mosbach.de').company-logo-wrap#dhbw-logo: img(src='../assets/dhbw-logo.png' alt='Cinteo company logo').company-logo
          .company-logo-text B.A. Online Media
        li.entry.enterprise
          a(target='_blank' href='http://blog.mercedes-benz-passion.com/2016/04/hack-stuttgart-50-studenten-24-stunden-zehn-ideen-drei-gewinner/').company-logo-wrap: img(src='../assets/ddl-logo.png' alt='Lesz company logo').company-logo
          .company-logo-text 1st Place Hack.Stuttgart 
        li.entry.enterprise
          a(target='_blank' href='https://hsg-eberbach.de').company-logo-wrap#dhbw-logo: img(src='../assets/hsg-logo.png' alt='HSG Eberbach company logo').company-logo
          .company-logo-text Student Art Award

    #callout Get in touch!

    section#Imprint: address
      h2: a(href='#Imprint') Imprint
      a.link(href='mailto:contact@jan-wirth.de') contact@jan-wirth.de
      .private Kurfürstenweg 10/1
      .private 69412 Eberbach

    footer: .print
      span.page-url jan-wirth.de
      span.page-number 3


</template>
<script>
import points from './Dots.vue'
import inlineList from './InlineList.vue'
export default {
  components: { points, inlineList }
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


.entry:not(:last-child) > .testimonal
  margin-bottom: 20px

h1
header
  white-space: nowrap
header
  height: 30px
  line-height: 30px

.entry
  min-height: 40px
  
.company-logo
  transform: translateX(-17px)

for child in 1 .. 10
  section:nth-of-type({child})
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

.skill-text
  z-index: 2000
  position: absolute
  pointer-events: none
  opacity: 0
  margin-top: 0
  transition: .1s
  background: white
  padding: 15px 15px 20px
  margin: -10px -15px

.entry:hover .skill-text
.skill:hover .skill-text
  transition-delay: .2s
  opacity: 1

section#intro
  transition-delay: 0
section:not(:hover)
  transition: .3s
  transition-delay: .3s

#skills
  z-index: 100

#experience
  z-index: 90

.enterprise .skill-text
  transform: translateY(75px)

address
  font-style: normal
  weigth: 0
  opacity: .5
  transition: .3s

address:hover
  opacity: 1

#callout
  font-size: 47px
  margin-bottom: -20px

#Imprint .private
  opacity: 0

#Imprint:target .private
  opacity: 1

#Education .company-logo
  transform: translateX(0)

.references
  display: flex
  justify-content: space-between
  padding-top: 10px

.reference
  display: block
  opacity: .7
.reference:hover
  opacity: 1
.reference img
  width: 30px
  height: 30px

</style>
