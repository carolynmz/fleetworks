<template>
  <section id="home" class="hero">
    <div class="hero-overlay"></div>
    <div class="hero-content">
      <h5 class="hero-subtitle">PROVIDING QUALITY TRUCK AND TRAILER REPAIR</h5>
      <h1 class="hero-title">FLEETWORKS</h1>
      <a href="#scheduleservice" class="cta-button">
        <span>▶</span> Schedule service
      </a>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  height: 100vh;
  min-height: 600px;
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
              url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><rect fill="%23333" width="1200" height="800"/></svg>');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-align: center;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 45, 91, 0.7);
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
  padding: 20px;
}

.hero-subtitle {
  font-size: 18px;
  font-weight: 400;
  letter-spacing: 2px;
  margin-bottom: 20px;
  text-transform: uppercase;
  animation: fadeInUp 1s ease;
}

.hero-title {
  font-size: 72px;
  font-weight: 700;
  letter-spacing: 4px;
  margin-bottom: 40px;
  animation: fadeInUp 1.2s ease;
}

.cta-button {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 15px 35px;
  background: #E74C3C;
  color: white;
  text-decoration: none;
  font-size: 16px;
  font-weight: 600;
  border-radius: 3px;
  transition: all 0.3s;
  animation: fadeInUp 1.4s ease;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.cta-button:hover {
  background: #C0392B;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(231, 76, 60, 0.4);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .hero {
    min-height: 500px;
    height: 70vh;
  }

  .hero-subtitle {
    font-size: 14px;
  }

  .hero-title {
    font-size: 42px;
  }

  .cta-button {
    padding: 12px 28px;
    font-size: 14px;
  }
}

@media (max-width: 480px) {
  .hero {
    min-height: 450px;
  }

  .hero-subtitle {
    font-size: 12px;
  }

  .hero-title {
    font-size: 32px;
  }
}
</style>
