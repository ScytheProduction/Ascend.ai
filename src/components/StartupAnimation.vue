<template>
  <div v-if="showAnimation" class="fixed inset-0 z-50 bg-[#fefefe] flex items-center justify-center" ref="animationOverlay">
    <div class="relative">
      <div class="logo-text text-7xl font-bold" ref="logo">Ascend.Pro</div>
      <div class="reveal-mask" ref="mask"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StartupAnimation',
  data() {
    return {
      showAnimation: true
    }
  },
  mounted() {
    // Check if animation has already been played
    try {
      const animationPlayed = localStorage.getItem('animationPlayed');

      if (animationPlayed) {
        // Skip animation, show main content immediately
        this.showAnimation = false;
        this.showMainContent();
        return;
      }
    } catch (e) {
      // localStorage disabled or error - continue with animation
      console.warn('localStorage not available:', e);
    }

    // Play animation sequence
    this.playAnimation();
  },
  methods: {
    playAnimation() {
      const logo = this.$refs.logo;
      const mask = this.$refs.mask;

      // Phase 1 (0-300ms): Logo appearance
      setTimeout(() => {
        if (logo) {
          logo.style.animation = 'logoAppear 0.3s ease-out forwards';
        }
      }, 0);

      // Phase 2 (300-900ms): Mask slide reveal
      setTimeout(() => {
        if (mask) {
          mask.style.animation = 'maskSlide 0.6s ease-out forwards';
        }
      }, 300);

      // Phase 3 (900-1200ms): Logo pulse
      setTimeout(() => {
        if (logo) {
          logo.style.animation = 'logoPulse 0.3s ease-in-out';
        }
      }, 900);

      // Phase 4 (1200-1700ms): Fade out overlay, fade in main content
      setTimeout(() => {
        const overlay = this.$refs.animationOverlay;
        if (overlay) {
          overlay.style.animation = 'fadeOut 0.5s ease-in-out forwards';
        }
        this.showMainContent();
      }, 1200);

      // Remove animation overlay from DOM and set localStorage flag
      setTimeout(() => {
        this.showAnimation = false;
        try {
          localStorage.setItem('animationPlayed', 'true');
        } catch (e) {
          console.warn('Could not set localStorage flag:', e);
        }
      }, 1700);
    },
    showMainContent() {
      // Show main content by setting opacity to 1
      const mainContent = document.getElementById('main-content');
      if (mainContent) {
        mainContent.style.opacity = '1';
      }
    }
  }
}
</script>

<style>
.logo-text {
  background: linear-gradient(135deg, #c026d3, #22d3ee, #a3e635);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 0;
  transform: scale(0.8);
}

.reveal-mask {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(254, 254, 254, 0.7);
  transform: translateX(100%);
}

@keyframes logoAppear {
  0% {
    opacity: 0;
    transform: scale(0.8);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes maskSlide {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}

@keyframes logoPulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes fadeOut {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
</style>
