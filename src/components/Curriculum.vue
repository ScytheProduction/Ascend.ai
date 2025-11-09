<template>
  <section class="py-20 px-5 bg-[#fafafa] relative" id="curriculum">
    <div class="text-center mb-20 max-w-7xl mx-auto">
      <h2 class="text-5xl font-bold mb-3 font-['Sora']">Your Learning Path</h2>
      <p class="text-lg text-gray-500">Three tiers to master AI monetization</p>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-7xl mx-auto">
      <div v-for="(tier, index) in tiers" :key="index" class="bg-gradient-to-br from-white to-gray-50 border-2 rounded-2xl p-8 transition-all hover:shadow-xl hover:-translate-y-1 relative" :class="tier.featured ? 'border-[#22d3ee] shadow-lg shadow-cyan-500/20' : 'border-gray-200'">
        <!-- Featured badge (only Tier 2) -->
        <div v-if="tier.featured" class="absolute -top-2.5 right-4 bg-gradient-to-r from-[#22d3ee] to-[#0891b2] text-white px-3 py-1 rounded-xl text-xs font-bold">
          MOST POPULAR
        </div>

        <!-- Tier icon shape -->
        <div :class="`tier-icon-${tier.color}`" class="mb-4"></div>

        <!-- Tier badge -->
        <div class="inline-block px-3 py-1.5 rounded-md text-xs font-semibold mb-4" :class="getTierBadgeClasses(tier.color)">
          {{ tier.badge }}
        </div>

        <!-- Tier title -->
        <h3 class="text-2xl font-bold mb-3" :class="getTierTitleColor(tier.color)">{{ tier.title }}</h3>

        <!-- Focus description -->
        <p class="text-gray-600 text-sm mb-6 leading-relaxed">{{ tier.focus }}</p>

        <!-- Key modules label -->
        <div class="text-xs text-gray-500 font-semibold uppercase tracking-wide mb-3">Key Modules</div>

        <!-- Module list -->
        <div class="flex flex-col gap-2.5 mb-6">
          <div v-for="(module, i) in tier.modules" :key="i" class="flex items-center gap-2 text-sm text-gray-700">
            <svg class="w-4 h-4 flex-shrink-0" :class="getTierIconColor(tier.color)" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path>
            </svg>
            <span>{{ module }}</span>
          </div>
        </div>

        <!-- Button -->
        <button class="w-full py-3.5 text-white rounded-xl font-semibold text-sm transition-all" :class="getTierButtonClasses(tier.color)">
          Start Learning
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Curriculum',
  data() {
    return {
      tiers: [
        {
          badge: 'Phase 1',
          title: 'AI Fundamentals for Rapid Income',
          focus: 'Leveraging accessible AI (ChatGPT, Midjourney) for high-leverage, immediate tasks',
          highlights: [
            'Automated content generation',
            'Market analysis & research',
            'Rapid prototyping',
            'Micro-service launch'
          ],
          outcome: 'Launching your first low-friction, high-margin AI service in under 14 days.',
          featured: false
        },
        {
          badge: 'Phase 2',
          title: 'AI E-commerce Automation',
          focus: 'Implementing AI for the entire e-commerce lifecycle on Shopify',
          highlights: [
            'Product research automation',
            'AI listing creation',
            'Dynamic ad copy generation',
            'AI customer service'
          ],
          outcome: 'An automated e-commerce engine that scales with minimal manual input.',
          featured: true
        },
        {
          badge: 'Phase 3',
          title: 'The AI Automation Agency',
          focus: 'Building and selling custom AI workflows to businesses',
          highlights: [
            'Zapier & Make integration',
            'Custom LLM deployment',
            'Workflow automation',
            'Retainer contracts'
          ],
          outcome: 'Launching a high-profit AI Automation Services business with $5k+ monthly retainers.',
          featured: false
        }
      ]
    }
  }
}
</script>

<style scoped>
.curriculum {
  background: linear-gradient(180deg, rgba(15, 26, 53, 0.5) 0%, rgba(10, 10, 10, 0.8) 100%);
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

.tiers {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 30px;
}

.tier-card {
  background: rgba(31, 41, 55, 0.3);
  border: 1px solid rgba(59, 130, 246, 0.1);
  border-radius: 16px;
  padding: 40px;
  transition: all 0.3s;
  position: relative;
  overflow: hidden;
}

.tier-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(59, 130, 246, 0.3), transparent);
}

.tier-card:hover {
  border-color: rgba(59, 130, 246, 0.3);
  transform: translateY(-8px);
  background: rgba(31, 41, 55, 0.5);
}

.tier-card.featured {
  border-color: rgba(59, 130, 246, 0.4);
  background: rgba(59, 130, 246, 0.05);
  transform: scale(1.02);
}

.tier-badge {
  display: inline-block;
  background: linear-gradient(135deg, rgba(59, 130, 246, 0.2), rgba(96, 165, 250, 0.2));
  color: #60a5fa;
  padding: 6px 14px;
  border-radius: 6px;
  font-size: 12px;
  font-weight: 600;
  margin-bottom: 16px;
  border: 1px solid rgba(59, 130, 246, 0.3);
}

.tier-title {
  font-size: 24px;
  margin-bottom: 12px;
}

.tier-focus {
  color: #9ca3af;
  font-size: 14px;
  margin-bottom: 28px;
  line-height: 1.6;
}

.tier-highlights {
  margin-bottom: 28px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.highlight {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 14px;
  color: #d1d5db;
}

.highlight-icon {
  color: #34d399;
  font-weight: 700;
  flex-shrink: 0;
}

.tier-outcome {
  background: rgba(59, 130, 246, 0.05);
  border: 1px solid rgba(59, 130, 246, 0.1);
  border-radius: 8px;
  padding: 16px;
  margin-bottom: 28px;
}

.outcome-label {
  font-size: 12px;
  color: #60a5fa;
  text-transform: uppercase;
  font-weight: 600;
  letter-spacing: 0.5px;
}

.tier-outcome p {
  font-size: 14px;
  color: #d1d5db;
  margin-top: 8px;
  line-height: 1.6;
}

.btn-tier {
  width: 100%;
  padding: 14px;
  background: rgba(59, 130, 246, 0.1);
  border: 1px solid rgba(59, 130, 246, 0.3);
  color: #60a5fa;
  border-radius: 10px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s;
}

.btn-tier:hover {
  background: rgba(59, 130, 246, 0.2);
  border-color: rgba(59, 130, 246, 0.5);
}

.btn-featured {
  background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
  color: white;
  border: none;
  box-shadow: 0 4px 20px rgba(59, 130, 246, 0.3);
}

.btn-featured:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 30px rgba(59, 130, 246, 0.4);
}

@media (max-width: 1024px) {
  .tiers {
    grid-template-columns: 1fr;
  }

  .tier-card.featured {
    transform: scale(1);
  }
}

@media (max-width: 768px) {
  .section-header h2 {
    font-size: 36px;
  }

  .tier-card {
    padding: 30px;
  }
}
</style>
