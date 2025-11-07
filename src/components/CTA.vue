<template>
  <section class="cta">
    <div class="container">
      <div class="cta-content">
        <div class="cta-text">
          <h2>Stop Learning Theory.<br>Start Generating Revenue.</h2>
          <p>Limited spots available for the next live Q&A with the Founder on scaling your first AI Automation client.</p>
        </div>
        <div class="cta-form">
          <input type="email" placeholder="Enter your email" class="input-email">
          <button class="btn btn-primary">Get Started Now</button>
          <p class="cta-note">No credit card required. Instant access to Tier 1.</p>
        </div>
      </div>
      <div class="social-proof">
        <p>Join 10,000+ AI entrepreneurs generating 6-figure income</p>
        <div class="avatars">
          <div v-for="i in 5" :key="i" class="avatar">{{ String.fromCharCode(65 + i) }}</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'CTA'
}
</script>

<style scoped>
.cta {
  background: radial-gradient(circle at top right, rgba(59, 130, 246, 0.15), transparent),
              radial-gradient(circle at bottom left, rgba(30, 64, 175, 0.1), transparent);
  border: 1px solid rgba(59, 130, 246, 0.2);
  border-radius: 20px;
  padding: 80px 40px;
  margin: 80px auto;
  max-width: 900px;
  position: relative;
  overflow: hidden;
}

.cta::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -50%;
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.1), transparent);
  border-radius: 50%;
  filter: blur(40px);
  z-index: 0;
}

.container {
  position: relative;
  z-index: 1;
}

.cta-content {
  text-align: center;
  margin-bottom: 60px;
}

.cta-text h2 {
  font-size: 42px;
  margin-bottom: 16px;
  line-height: 1.3;
}

.cta-text p {
  color: #9ca3af;
  font-size: 16px;
  margin-bottom: 40px;
}

.cta-form {
  display: flex;
  gap: 12px;
  max-width: 500px;
  margin: 0 auto 20px;
  flex-wrap: wrap;
  justify-content: center;
}

.input-email {
  flex: 1;
  min-width: 250px;
  padding: 16px 20px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  color: white;
  font-size: 14px;
  transition: all 0.3s;
}

.input-email::placeholder {
  color: #6b7280;
}

.input-email:focus {
  outline: none;
  border-color: rgba(59, 130, 246, 0.5);
  background: rgba(255, 255, 255, 0.08);
}

.btn {
  padding: 16px 40px;
  border: none;
  border-radius: 10px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s;
}

.btn-primary {
  background: linear-gradient(135deg, #3b82f6 0%, #1e40af 100%);
  color: white;
  box-shadow: 0 4px 15px rgba(59, 130, 246, 0.3);
  white-space: nowrap;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(59, 130, 246, 0.4);
}

.cta-note {
  font-size: 12px;
  color: #6b7280;
}

.social-proof {
  text-align: center;
}

.social-proof p {
  font-size: 14px;
  color: #9ca3af;
  margin-bottom: 16px;
}

.avatars {
  display: flex;
  justify-content: center;
  gap: -8px;
}

.avatar {
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: linear-gradient(135deg, #3b82f6, #1e40af);
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: 700;
  font-size: 14px;
  border: 2px solid rgba(10, 10, 10, 0.9);
  margin-left: -8px;
}

.avatar:first-child {
  margin-left: 0;
}

@media (max-width: 768px) {
  .cta {
    padding: 60px 30px;
    margin: 60px 20px;
  }

  .cta-text h2 {
    font-size: 32px;
  }

  .cta-form {
    flex-direction: column;
  }

  .input-email {
    min-width: 100%;
  }

  .btn {
    width: 100%;
  }
}
</style>
