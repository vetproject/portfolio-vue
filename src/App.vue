<template>
  <IntroPort msg="Welcome to Your Vue.js App"/>
  <About />
  <EducationPort />
  <SkillsPort />
  <ProjectsPort />
  <Contact />
  <FooterPort />
</template>

<script>
import IntroPort from './components/Intro.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import FooterPort from './components/Footer.vue'
import EducationPort from './components/Education.vue'
import SkillsPort from './components/Skills.vue'
import ProjectsPort from './components/Projects.vue'

export default {
  name: 'App',
  components: {
    IntroPort,
    About,
    Contact,
    FooterPort,
    EducationPort,
    SkillsPort,
    ProjectsPort
  }
}
</script>

<style>

</style>
