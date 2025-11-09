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

<style>
.feature-icon {
  animation: bounce 3s ease-in-out infinite;
}

.bg-white:nth-child(2) .feature-icon {
  animation-delay: 0.2s;
}

.bg-white:nth-child(3) .feature-icon {
  animation-delay: 0.4s;
}

.bg-white:nth-child(4) .feature-icon {
  animation-delay: 0.6s;
}

.bg-white:nth-child(5) .feature-icon {
  animation-delay: 0.8s;
}

.bg-white:nth-child(6) .feature-icon {
  animation-delay: 1s;
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}
</style>
