<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-section">
          <h4>AI Profit</h4>
          <p>Master the blueprint for high-demand AI ventures and build your six-figure business.</p>
        </div>
        <div class="footer-section">
          <h4>Curriculum</h4>
          <ul>
            <li><a href="#curriculum">Phase 1: Fundamentals</a></li>
            <li><a href="#curriculum">Phase 2: E-commerce</a></li>
            <li><a href="#curriculum">Phase 3: Automation Agency</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Company</h4>
          <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Privacy</a></li>
          </ul>
        </div>
        <div class="footer-section">
          <h4>Community</h4>
          <ul>
            <li><a href="#">Discord</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">LinkedIn</a></li>
            <li><a href="#">Newsletter</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 AI Profit. All rights reserved.</p>
        <div class="footer-links">
          <a href="#">Terms of Service</a>
          <span>·</span>
          <a href="#">Privacy Policy</a>
          <span>·</span>
          <a href="#">Cookie Policy</a>
        </div>
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
