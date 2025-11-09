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

<style scoped>
.header {
  position: sticky;
  top: 0;
  background: rgba(10, 10, 10, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid rgba(31, 41, 55, 0.3);
  z-index: 100;
  padding: 20px 0;
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 24px;
  font-weight: 700;
  cursor: pointer;
  transition: transform 0.3s;
}

.logo:hover {
  transform: scale(1.05);
}

.logo-icon {
  font-size: 28px;
}

.logo-text {
  background: linear-gradient(135deg, #3b82f6 0%, #60a5fa 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 40px;
}

.nav-links a {
  color: #9ca3af;
  text-decoration: none;
  font-size: 14px;
  font-weight: 500;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #3b82f6;
}

.btn {
  padding: 10px 24px;
  border: none;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s;
}

.btn-primary {
  background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
  color: white;
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(59, 130, 246, 0.4);
}

@media (max-width: 768px) {
  .nav-links {
    gap: 20px;
  }

  .nav-links a {
    display: none;
  }
}
</style>
