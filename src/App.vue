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
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Curriculum from './components/Curriculum.vue'
import Features from './components/Features.vue'
import CTA from './components/CTA.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
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

:root {
  --black: #0a0a0a;
  --dark-blue: #0f1a35;
  --accent-blue: #1e40af;
  --light-blue: #3b82f6;
  --neutral-800: #1a1a1a;
  --neutral-600: #4b5563;
  --neutral-400: #9ca3af;
  --white: #ffffff;
  --surface: #111827;
  --border: #1f2937;
}

body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, var(--black) 0%, var(--dark-blue) 100%);
  color: var(--white);
  line-height: 1.6;
}

.app {
  min-height: 100vh;
  background: linear-gradient(135deg, var(--black) 0%, var(--dark-blue) 100%);
}

h1, h2, h3, h4, h5, h6 {
  font-family: 'Sora', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  font-weight: 700;
  line-height: 1.2;
}

section {
  padding: 80px 20px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

@media (max-width: 768px) {
  section {
    padding: 60px 20px;
  }
}
</style>
