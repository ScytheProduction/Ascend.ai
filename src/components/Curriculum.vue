<template>
  <section class="curriculum" id="curriculum">
    <div class="container">
      <div class="section-header">
        <h2>Your AI Profit Ascent</h2>
        <p>From Beginner to Capitalist</p>
      </div>
      <div class="tiers">
        <div v-for="(tier, index) in tiers" :key="index" class="tier-card" :class="{ featured: tier.featured }">
          <div class="tier-badge">{{ tier.badge }}</div>
          <h3 class="tier-title">{{ tier.title }}</h3>
          <p class="tier-focus">{{ tier.focus }}</p>
          <div class="tier-highlights">
            <div v-for="(highlight, i) in tier.highlights" :key="i" class="highlight">
              <span class="highlight-icon">✓</span>
              <span>{{ highlight }}</span>
            </div>
          </div>
          <div class="tier-outcome">
            <span class="outcome-label">Outcome:</span>
            <p>{{ tier.outcome }}</p>
          </div>
          <button class="btn btn-tier" :class="{ 'btn-featured': tier.featured }">
            {{ tier.featured ? 'Start Now' : 'Learn More' }}
          </button>
        </div>
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
