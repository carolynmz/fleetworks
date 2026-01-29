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
          <div class="image-float image-1">
            <IconTools :size="50" class="float-icon" />
          </div>
          <div class="image-float image-2">
            <IconTools :size="50" class="float-icon" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { IconTools } from '@tabler/icons-vue'
</script>

<style lang="scss" scoped>
$primary-color: #002D5B;
$accent-color: #E74C3C;
$gray-dark: #555;
$gray-darkest: #95a5a6;
$gray-darker: #7f8c8d;
$white: white;

.about-us {
  padding: 80px 0;
  background: $white;
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

.about-text {
  h2 {
    font-size: 36px;
    font-weight: 700;
    color: $primary-color;
    margin-bottom: 25px;
    line-height: 1.3;
  }

  p {
    font-size: 16px;
    line-height: 1.8;
    color: $gray-dark;
  }
}

.divider {
  width: 80px;
  height: 4px;
  background: $accent-color;
  margin-bottom: 25px;
}

.about-images {
  position: relative;
  height: 400px;
}

.image-float {
  position: absolute;
  background: linear-gradient(135deg, $gray-darkest 0%, $gray-darker 100%);
  border-radius: 8px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;

  &:hover {
    transform: translateY(-5px);
  }
}

.float-icon {
  opacity: 0.3;
  color: $white;
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

  .about-text {
    h2 {
      font-size: 26px;
    }

    p {
      font-size: 15px;
    }
  }

  .about-images {
    height: 300px;
    margin: 0 auto;
    max-width: 400px;
  }
}

@media (max-width: 480px) {
  .about-text {
    h2 {
      font-size: 22px;
    }

    p {
      font-size: 14px;
    }
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
