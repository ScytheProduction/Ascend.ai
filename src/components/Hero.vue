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

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: 80px 20px;
  position: relative;
  overflow: hidden;
}

.hero-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.hero-text {
  z-index: 10;
}

.hero-title {
  font-size: 56px;
  line-height: 1.2;
  margin-bottom: 24px;
  font-weight: 700;
}

.gradient-text {
  background: linear-gradient(135deg, #3b82f6 0%, #60a5fa 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-subtitle {
  font-size: 18px;
  color: #9ca3af;
  margin-bottom: 40px;
  line-height: 1.8;
  max-width: 500px;
}

.hero-cta {
  display: flex;
  gap: 20px;
  margin-bottom: 60px;
  flex-wrap: wrap;
}

.btn {
  padding: 16px 32px;
  border: none;
  border-radius: 12px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s;
}

.btn-lg {
  padding: 16px 40px;
}

.btn-primary {
  background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
  color: white;
  box-shadow: 0 10px 40px rgba(59, 130, 246, 0.3);
}

.btn-primary:hover {
  transform: translateY(-4px);
  box-shadow: 0 15px 50px rgba(59, 130, 246, 0.4);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.1);
  color: white;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.15);
  border-color: rgba(255, 255, 255, 0.3);
  transform: translateY(-4px);
}

.hero-stats {
  display: flex;
  gap: 60px;
}

.stat {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.stat-number {
  font-size: 28px;
  font-weight: 700;
  color: #3b82f6;
}

.stat-label {
  font-size: 14px;
  color: #6b7280;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.hero-visual {
  position: relative;
  height: 500px;
}

.gradient-orb {
  position: absolute;
  border-radius: 50%;
  opacity: 0.3;
  filter: blur(40px);
}

.orb-1 {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
  top: 50px;
  right: 100px;
  animation: float 6s ease-in-out infinite;
}

.orb-2 {
  width: 250px;
  height: 250px;
  background: linear-gradient(135deg, #60a5fa 0%, #3b82f6 100%);
  bottom: 50px;
  left: 50px;
  animation: float 8s ease-in-out infinite reverse;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(30px); }
}

.code-window {
  position: absolute;
  bottom: 20px;
  right: 20px;
  background: rgba(15, 26, 53, 0.8);
  border: 1px solid rgba(59, 130, 246, 0.2);
  border-radius: 12px;
  overflow: hidden;
  backdrop-filter: blur(10px);
  width: 100%;
  max-width: 400px;
}

.code-header {
  display: flex;
  gap: 8px;
  padding: 12px 16px;
  background: rgba(0, 0, 0, 0.3);
  border-bottom: 1px solid rgba(59, 130, 246, 0.1);
}

.code-header span {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.2);
}

.code-content {
  padding: 20px;
  font-family: 'Monaco', 'Courier New', monospace;
  font-size: 13px;
  line-height: 1.8;
}

.code-line {
  color: #d1d5db;
}

.code-indent {
  margin-left: 20px;
}

.token-keyword {
  color: #3b82f6;
}

.token-punc {
  color: #9ca3af;
}

.token-number {
  color: #34d399;
}

@media (max-width: 1024px) {
  .hero-content {
    grid-template-columns: 1fr;
  }

  .hero-visual {
    height: 300px;
  }

  .hero-title {
    font-size: 42px;
  }
}

@media (max-width: 768px) {
  .hero-cta {
    flex-direction: column;
  }

  .hero-stats {
    gap: 30px;
  }

  .hero-title {
    font-size: 32px;
  }
}
</style>
