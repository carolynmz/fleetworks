<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="container">
        <div class="footer-grid">
          <div class="footer-col">
            <h4>About Us</h4>
            <p>We are a private repair shop located in Richfield, Ohio, right off I271 and I71. We speak English and Ukrainian!</p>
          </div>

          <div class="footer-col">
            <h4>Contact info</h4>
            <p><strong>Address:</strong> 3024 Brecksville Rd Ste B Richfield, Ohio 44286</p>
            <p><strong>Phone:</strong> (440)829-2132</p>
            <p><strong>E-mail:</strong> fleetworksmain@gmail.com</p>
          </div>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="container">
        <p>Copyright &copy; 2025. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: #002D5B;
  color: white;
}

.footer-content {
  padding: 60px 0 40px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
}

.footer-col h4 {
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 20px;
  text-transform: uppercase;
}

.footer-col p {
  font-size: 14px;
  line-height: 1.8;
  color: rgba(255, 255, 255, 0.9);
  margin-bottom: 10px;
}

.footer-bottom {
  background: rgba(0, 0, 0, 0.2);
  padding: 20px 0;
  text-align: center;
}

.footer-bottom p {
  font-size: 13px;
  color: rgba(255, 255, 255, 0.8);
  margin: 0;
}

@media (max-width: 768px) {
  .footer-content {
    padding: 40px 0 30px;
  }

  .footer-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .footer-col h4 {
    font-size: 18px;
  }

  .footer-col p {
    font-size: 13px;
  }
}

@media (max-width: 480px) {
  .footer-content {
    padding: 30px 0 20px;
  }

  .footer-col h4 {
    font-size: 16px;
  }

  .footer-col p {
    font-size: 12px;
  }

  .footer-bottom p {
    font-size: 12px;
  }
}
</style>
