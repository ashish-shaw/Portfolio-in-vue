<template>
  <div id="app">
    <Header/>
    <Portfolio/>
    <About/>
    <Projects/>
    <Skills/>
    <Contact/>
  </div>
</template>

<script>
import Portfolio from './components/Portfolio.vue'
import Header from './components/Header.vue'
import About from './components/AboutSection.vue'
import Projects from './components/ProjectSection.vue'
import Skills from './components/SkillSet.vue'
import Contact from './components/ContactSection.vue'
export default {
  name: 'App',
  components: {
    Portfolio,
    Header,
    About,
    Projects,
    Skills,
    Contact
  }
}
</script>
