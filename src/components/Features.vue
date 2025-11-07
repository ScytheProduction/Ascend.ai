<template>
  <section class="features" id="features">
    <div class="container">
      <div class="section-header">
        <h2>Why Our Curriculum Works</h2>
        <p>The Profit Advantage</p>
      </div>
      <div class="features-grid">
        <div v-for="(feature, index) in features" :key="index" class="feature-card">
          <div class="feature-icon">{{ feature.icon }}</div>
          <h3>{{ feature.title }}</h3>
          <p>{{ feature.description }}</p>
        </div>
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
