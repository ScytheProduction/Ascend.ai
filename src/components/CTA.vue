<template>
  <section class="bg-gradient-to-br from-fuchsia-50 to-cyan-50 border-2 border-fuchsia-200 rounded-3xl py-20 px-10 my-20 mx-auto max-w-4xl relative overflow-hidden">
    <div class="text-center mb-15 relative z-10">
      <h2 class="text-4xl md:text-5xl font-bold mb-4 leading-tight font-['Sora']">Ready to Master AI Funnels?</h2>
      <p class="text-gray-600 text-base mb-10">Join thousands learning to automate and scale with AI-powered marketing.</p>
      <div class="flex gap-3 max-w-lg mx-auto mb-5 flex-wrap justify-center">
        <input type="email" placeholder="Enter your email" class="flex-1 min-w-[250px] px-5 py-4 bg-white border border-gray-300 rounded-xl text-gray-900 text-sm focus:outline-none focus:border-[#22d3ee] focus:ring-2 focus:ring-cyan-500/20 transition-all">
        <button class="px-10 py-4 bg-gradient-to-r from-[#22d3ee] to-[#0891b2] text-white rounded-xl font-semibold text-sm shadow-lg shadow-cyan-500/30 hover:-translate-y-0.5 hover:shadow-xl transition-all whitespace-nowrap">Start Your Free Trial</button>
      </div>
      <p class="text-xs text-gray-500">No credit card required. Instant access to Tier 1.</p>
    </div>
    <div class="text-center relative z-10">
      <p class="text-sm text-gray-600 mb-4">Join 10,000+ AI entrepreneurs generating 6-figure income</p>
      <div class="flex justify-center">
        <div v-for="i in 5" :key="i" class="w-10 h-10 rounded-full bg-gradient-to-r from-[#c026d3] to-[#9333ea] flex items-center justify-center text-white font-bold text-sm border-2 border-white -ml-2 first:ml-0">{{ String.fromCharCode(65 + i) }}</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'CTA'
}
</script>

<style>
/* Optional: Add subtle glow effect */
</style>
