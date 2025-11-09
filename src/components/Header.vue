<template>
  <header class="sticky top-0 z-50 bg-white/95 backdrop-blur-md border-b border-gray-200 py-5">
    <div class="flex justify-between items-center max-w-7xl mx-auto px-5">
      <div class="flex items-center gap-2.5 text-2xl font-bold cursor-pointer transition-transform hover:scale-105">
        <span class="text-3xl">⚡</span>
        <span class="logo-text">Ascend.Pro</span>
      </div>
      <nav class="flex items-center gap-10">
        <a href="#curriculum" class="hidden md:inline-block text-gray-500 text-sm font-medium hover:text-[#c026d3] transition-colors">Curriculum</a>
        <a href="#features" class="hidden md:inline-block text-gray-500 text-sm font-medium hover:text-[#c026d3] transition-colors">Features</a>
        <button class="px-6 py-2.5 bg-gradient-to-r from-[#22d3ee] to-[#0891b2] text-white rounded-lg font-semibold text-sm shadow-lg shadow-cyan-500/30 hover:-translate-y-0.5 hover:shadow-xl hover:shadow-cyan-500/40 transition-all">Start Free</button>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style>
.logo-text {
  background: linear-gradient(135deg, #c026d3, #22d3ee);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
</style>
