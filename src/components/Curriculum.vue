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
          badge: 'TIER 1',
          title: 'Foundation Explorer',
          focus: 'Focus on Core Setup. Learn to build landing pages, integrate basic AI content generation (headlines, email copy), and structure a simple sales funnel.',
          modules: [
            'AI Copywriting Essentials',
            'Landing Page Architecture',
            'Basic Email Automation'
          ],
          color: 'magenta',
          featured: false
        },
        {
          badge: 'TIER 2',
          title: 'Profit Accelerator',
          focus: 'Focus on Optimization & Scaling. Deep dive into advanced AI-driven audience segmentation, A/B testing, and building complex, multi-stage funnels with upsells/downsells.',
          modules: [
            'Advanced Prompt Engineering',
            'Data-Driven Funnel Optimization',
            'Personalized AI Outreach'
          ],
          color: 'cyan',
          featured: true
        },
        {
          badge: 'TIER 3',
          title: 'Autonomous Architect',
          focus: 'Focus on Full Automation & Strategy. Master connecting multiple AI services, setting up automated product creation (e.g., course outlines, eBooks), and running the business on autopilot.',
          modules: [
            'RAG Implementation for Content',
            'Autonomous Lead Scoring',
            'Platform Integration Mastery'
          ],
          color: 'lime',
          featured: false
        }
      ]
    }
  },
  methods: {
    getTierBadgeClasses(color) {
      const colors = {
        magenta: 'bg-fuchsia-100 text-fuchsia-700',
        cyan: 'bg-cyan-100 text-cyan-700',
        lime: 'bg-lime-100 text-lime-700'
      };
      return colors[color];
    },
    getTierTitleColor(color) {
      const colors = {
        magenta: 'text-[#c026d3]',
        cyan: 'text-[#0891b2]',
        lime: 'text-[#65a30d]'
      };
      return colors[color];
    },
    getTierIconColor(color) {
      const colors = {
        magenta: 'text-[#c026d3]',
        cyan: 'text-[#0891b2]',
        lime: 'text-[#65a30d]'
      };
      return colors[color];
    },
    getTierButtonClasses(color) {
      const colors = {
        magenta: 'bg-gradient-to-r from-[#c026d3] to-[#9333ea] hover:shadow-lg hover:-translate-y-0.5',
        cyan: 'bg-gradient-to-r from-[#22d3ee] to-[#0891b2] hover:shadow-lg hover:-translate-y-0.5',
        lime: 'bg-gradient-to-r from-[#a3e635] to-[#65a30d] hover:shadow-lg hover:-translate-y-0.5'
      };
      return colors[color];
    }
  }
}
</script>

<style>
/* Tier icon shapes */
.tier-icon-magenta {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, #c026d3, #9333ea);
  clip-path: polygon(30% 0%, 70% 0%, 100% 30%, 100% 70%, 70% 100%, 30% 100%, 0% 70%, 0% 30%);
}

.tier-icon-cyan {
  width: 50px;
  height: 50px;
  background: radial-gradient(circle at 30% 30%, #22d3ee, #0891b2);
  border-radius: 50%;
}

.tier-icon-lime {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, #a3e635, #65a30d);
  transform: rotate(45deg);
  clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
}
</style>
