<template>
  <section id="aboutus" class="about-us">
    <div class="container">
      <div class="about-content">
        <div class="about-text">
          <h2>We offer services for components of these manufacturers</h2>
          <div class="divider"></div>
          <p>Under orange line: Fleetworks puts a heavy emphasis on diagnosing and pinpointing the problem. This ensures that what's needed to be changed is changed and done right the first time.</p>
        </div>
        <div class="about-images">
          <div class="image-float image-1"></div>
          <div class="image-float image-2"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-us {
  padding: 80px 0;
  background: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.about-text h2 {
  font-size: 36px;
  font-weight: 700;
  color: #002D5B;
  margin-bottom: 25px;
  line-height: 1.3;
}

.divider {
  width: 80px;
  height: 4px;
  background: #E74C3C;
  margin-bottom: 25px;
}

.about-text p {
  font-size: 16px;
  line-height: 1.8;
  color: #555;
}

.about-images {
  position: relative;
  height: 400px;
}

.image-float {
  position: absolute;
  background: linear-gradient(135deg, #95a5a6 0%, #7f8c8d 100%);
  border-radius: 8px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease;
}

.image-float::after {
  content: '🔧';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 50px;
  opacity: 0.3;
}

.image-1 {
  width: 70%;
  height: 250px;
  top: 0;
  left: 0;
  z-index: 2;
}

.image-2 {
  width: 70%;
  height: 250px;
  bottom: 0;
  right: 0;
  z-index: 1;
}

.image-float:hover {
  transform: translateY(-5px);
}

@media (max-width: 1024px) {
  .about-content {
    gap: 40px;
  }

  .about-text h2 {
    font-size: 30px;
  }

  .about-images {
    height: 350px;
  }

  .image-1,
  .image-2 {
    height: 220px;
  }
}

@media (max-width: 768px) {
  .about-us {
    padding: 60px 0;
  }

  .about-content {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .about-text h2 {
    font-size: 26px;
  }

  .about-text p {
    font-size: 15px;
  }

  .about-images {
    height: 300px;
    margin: 0 auto;
    max-width: 400px;
  }
}

@media (max-width: 480px) {
  .about-text h2 {
    font-size: 22px;
  }

  .about-text p {
    font-size: 14px;
  }

  .about-images {
    height: 250px;
  }

  .image-1,
  .image-2 {
    height: 180px;
  }
}
</style>
