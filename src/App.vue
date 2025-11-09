<template>
  <div class="min-h-screen bg-[#fefefe] text-gray-900 font-['Inter'] relative overflow-x-hidden">
    <StartupAnimation />
    <div id="main-content" class="opacity-0 transition-opacity duration-500">
      <Header />
      <Hero />
      <Curriculum />
      <Features />
      <CTA />
      <Footer />
    </div>
  </div>
</template>

<script>
import StartupAnimation from './components/StartupAnimation.vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Curriculum from './components/Curriculum.vue'
import Features from './components/Features.vue'
import CTA from './components/CTA.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    StartupAnimation,
    Header,
    Hero,
    Curriculum,
    Features,
    CTA,
    Footer
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Sora', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}
</style>
