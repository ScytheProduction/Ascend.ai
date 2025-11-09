<template>
  <footer class="bg-gradient-to-b from-gray-50 to-gray-100 border-t border-gray-200 pt-20 pb-10 px-5">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-15 mb-15 max-w-7xl mx-auto">
      <div>
        <h4 class="text-base font-semibold mb-5">Ascend.Pro</h4>
        <p class="text-gray-600 text-sm leading-relaxed">Master AI-powered funnels and marketing automation to scale your online business.</p>
      </div>
      <div>
        <h4 class="text-base font-semibold mb-5">Curriculum</h4>
        <ul class="list-none">
          <li class="mb-3"><a href="#curriculum" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Tier 1: Foundation Explorer</a></li>
          <li class="mb-3"><a href="#curriculum" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Tier 2: Profit Accelerator</a></li>
          <li class="mb-3"><a href="#curriculum" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Tier 3: Autonomous Architect</a></li>
        </ul>
      </div>
      <div>
        <h4 class="text-base font-semibold mb-5">Company</h4>
        <ul class="list-none">
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">About</a></li>
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Blog</a></li>
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Contact</a></li>
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Privacy</a></li>
        </ul>
      </div>
      <div>
        <h4 class="text-base font-semibold mb-5">Community</h4>
        <ul class="list-none">
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Discord</a></li>
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Twitter</a></li>
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">LinkedIn</a></li>
          <li class="mb-3"><a href="#" class="text-gray-600 text-sm hover:text-[#c026d3] transition-colors">Newsletter</a></li>
        </ul>
      </div>
    </div>
    <div class="border-t border-gray-200 pt-10 flex justify-between items-center flex-wrap gap-5 max-w-7xl mx-auto">
      <p class="text-gray-500 text-xs">&copy; 2024 Ascend.Pro. All rights reserved.</p>
      <div class="flex items-center gap-3 text-xs">
        <a href="#" class="text-gray-500 hover:text-gray-700 transition-colors">Terms of Service</a>
        <span class="text-gray-400">·</span>
        <a href="#" class="text-gray-500 hover:text-gray-700 transition-colors">Privacy Policy</a>
        <span class="text-gray-400">·</span>
        <a href="#" class="text-gray-500 hover:text-gray-700 transition-colors">Cookie Policy</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
.footer {
  background: linear-gradient(180deg, rgba(10, 10, 10, 0.5) 0%, rgba(10, 10, 10, 0.9) 100%);
  border-top: 1px solid rgba(59, 130, 246, 0.1);
  padding: 80px 20px 40px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 60px;
  margin-bottom: 60px;
}

.footer-section h4 {
  font-size: 16px;
  margin-bottom: 20px;
  font-weight: 600;
}

.footer-section p {
  color: #9ca3af;
  font-size: 14px;
  line-height: 1.6;
}

.footer-section ul {
  list-style: none;
}

.footer-section li {
  margin-bottom: 12px;
}

.footer-section a {
  color: #9ca3af;
  text-decoration: none;
  font-size: 14px;
  transition: color 0.3s;
}

.footer-section a:hover {
  color: #3b82f6;
}

.footer-bottom {
  border-top: 1px solid rgba(59, 130, 246, 0.1);
  padding-top: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
}

.footer-bottom p {
  color: #6b7280;
  font-size: 13px;
}

.footer-links {
  display: flex;
  align-items: center;
  gap: 12px;
  font-size: 13px;
}

.footer-links a {
  color: #6b7280;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-links a:hover {
  color: #9ca3af;
}

.footer-links span {
  color: #4b5563;
}

@media (max-width: 768px) {
  .footer-content {
    gap: 40px;
  }

  .footer-bottom {
    flex-direction: column;
    text-align: center;
  }

  .footer-links {
    justify-content: center;
  }
}
</style>
