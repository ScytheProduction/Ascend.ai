<template>
  <section class="py-20 px-5 relative" id="features">
    <div class="text-center mb-20 max-w-7xl mx-auto">
      <h2 class="text-5xl font-bold mb-3 font-['Sora']">Why Our Curriculum Works</h2>
      <p class="text-lg text-gray-500">The Profit Advantage</p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10 max-w-7xl mx-auto">
      <div v-for="(feature, index) in features" :key="index" class="bg-white border-2 border-gray-200 rounded-xl p-10 transition-all hover:border-[#c026d3] hover:-translate-y-1 hover:shadow-lg text-center relative">
        <div class="feature-icon text-5xl mb-5 inline-block">{{ feature.icon }}</div>
        <h3 class="text-xl font-semibold mb-3">{{ feature.title }}</h3>
        <p class="text-gray-600 text-sm leading-relaxed">{{ feature.description }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Features',
  data() {
    return {
      features: [
        {
          icon: '⚙️',
          title: 'Tool-Agnostic & Actionable',
          description: 'Focused on the strategy of profit, not just specific apps. Learn how to use any AI tool to maximize efficiency and client results.'
        },
        {
          icon: '📈',
          title: 'The Progressive Path',
          description: 'No random videos. Our courses are structured to build upon each other, guaranteeing you acquire skills that directly translate to higher revenue.'
        },
        {
          icon: '🤝',
          title: 'Community & Support',
          description: 'Access to an exclusive community of AI entrepreneurs actively implementing and scaling the same profit strategies.'
        },
        {
          icon: '⚡',
          title: 'Real-World Projects',
          description: 'Build actual projects from day one. Apply every concept immediately to create tangible business results.'
        },
        {
          icon: '🔐',
          title: 'Lifetime Access',
          description: 'Once enrolled, you have forever access to all course materials, including future updates and new content.'
        },
        {
          icon: '💰',
          title: 'Money-Back Guarantee',
          description: 'Complete the first tier and don\'t see results? We\'ll give you your money back, no questions asked.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.features {
  position: relative;
}

.section-header {
  text-align: center;
  margin-bottom: 80px;
}

.section-header h2 {
  font-size: 48px;
  margin-bottom: 12px;
}

.section-header p {
  font-size: 18px;
  color: #9ca3af;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 40px;
}

.feature-card {
  background: rgba(31, 41, 55, 0.2);
  border: 1px solid rgba(59, 130, 246, 0.1);
  border-radius: 12px;
  padding: 40px;
  transition: all 0.3s;
  text-align: center;
  position: relative;
}

.feature-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(59, 130, 246, 0.2), transparent);
}

.feature-card:hover {
  border-color: rgba(59, 130, 246, 0.3);
  background: rgba(31, 41, 55, 0.4);
  transform: translateY(-4px);
}

.feature-icon {
  font-size: 48px;
  margin-bottom: 20px;
  display: inline-block;
  animation: bounce 3s ease-in-out infinite;
}

.feature-card:nth-child(2) .feature-icon {
  animation-delay: 0.2s;
}

.feature-card:nth-child(3) .feature-icon {
  animation-delay: 0.4s;
}

.feature-card:nth-child(4) .feature-icon {
  animation-delay: 0.6s;
}

.feature-card:nth-child(5) .feature-icon {
  animation-delay: 0.8s;
}

.feature-card:nth-child(6) .feature-icon {
  animation-delay: 1s;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

.feature-card h3 {
  font-size: 20px;
  margin-bottom: 12px;
}

.feature-card p {
  color: #9ca3af;
  font-size: 14px;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .section-header h2 {
    font-size: 36px;
  }

  .features-grid {
    grid-template-columns: 1fr;
    gap: 30px;
  }

  .feature-card {
    padding: 30px;
  }
}
</style>
