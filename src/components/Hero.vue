<template>
  <section class="min-h-screen flex items-center py-20 px-5 relative overflow-hidden">
    <!-- Background geometric shapes -->
    <div class="shape-octagon"></div>
    <div class="shape-sphere"></div>
    <div class="shape-diamond"></div>
    <div class="shape-ring"></div>

    <div class="grid md:grid-cols-2 gap-15 items-center max-w-7xl mx-auto w-full relative z-10">
      <div>
        <h1 class="text-5xl lg:text-6xl leading-tight mb-6 font-bold font-['Sora']">
          Master the Funnel: <span class="gradient-text">AI-Powered Profits.</span>
        </h1>
        <p class="text-lg text-gray-600 mb-10 leading-relaxed max-w-xl">
          Learn to seamlessly integrate generative AI into your marketing stack, automate sales, and scale your online business using platforms like Kartra and Kajabi.
        </p>
        <div class="flex gap-5 mb-15 flex-wrap">
          <button class="px-10 py-4 bg-gradient-to-r from-[#22d3ee] to-[#0891b2] text-white rounded-xl font-semibold text-base shadow-xl shadow-cyan-500/30 hover:-translate-y-1 hover:shadow-2xl hover:shadow-cyan-500/40 transition-all">Start Your Free Trial</button>
          <button class="px-10 py-4 bg-gray-100 text-gray-700 border border-gray-300 rounded-xl font-semibold hover:bg-gray-200 hover:-translate-y-1 transition-all">Watch Demo</button>
        </div>
        <div class="flex gap-15">
          <div class="flex flex-col gap-2">
            <span class="text-3xl font-bold text-[#c026d3]">10,000+</span>
            <span class="text-sm text-gray-500 uppercase tracking-wide">Students</span>
          </div>
          <div class="flex flex-col gap-2">
            <span class="text-3xl font-bold text-[#c026d3]">$5M+</span>
            <span class="text-sm text-gray-500 uppercase tracking-wide">Generated</span>
          </div>
          <div class="flex flex-col gap-2">
            <span class="text-3xl font-bold text-[#c026d3]">4.9★</span>
            <span class="text-sm text-gray-500 uppercase tracking-wide">Rating</span>
          </div>
        </div>
      </div>
      <div></div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style>
.gradient-text {
  background: linear-gradient(135deg, #c026d3, #22d3ee);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

/* Geometric background shapes */
.shape-octagon {
  position: absolute;
  width: 100px;
  height: 100px;
  top: 12%;
  left: 10%;
  opacity: 0.18;
  background: linear-gradient(135deg, #c026d3, #9333ea);
  clip-path: polygon(30% 0%, 70% 0%, 100% 30%, 100% 70%, 70% 100%, 30% 100%, 0% 70%, 0% 30%);
  box-shadow: 10px 10px 30px rgba(192, 38, 211, 0.15);
  pointer-events: none;
  z-index: 1;
}

.shape-sphere {
  position: absolute;
  width: 90px;
  height: 90px;
  top: 55%;
  right: 8%;
  opacity: 0.18;
  background: radial-gradient(circle at 30% 30%, #22d3ee, #0891b2);
  border-radius: 50%;
  box-shadow: 8px 8px 25px rgba(6, 182, 212, 0.2);
  pointer-events: none;
  z-index: 1;
}

.shape-diamond {
  position: absolute;
  width: 110px;
  height: 110px;
  bottom: 18%;
  left: 20%;
  opacity: 0.18;
  background: linear-gradient(135deg, #a3e635, #65a30d);
  transform: rotate(45deg);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
  box-shadow: 12px 12px 35px rgba(132, 204, 22, 0.18);
  pointer-events: none;
  z-index: 1;
}

.shape-ring {
  position: absolute;
  width: 80px;
  height: 80px;
  top: 40%;
  right: 35%;
  opacity: 0.25;
  border: 3px solid #f97316;
  border-radius: 50%;
  pointer-events: none;
  z-index: 1;
}
</style>
