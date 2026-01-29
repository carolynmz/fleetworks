<template>
  <section id="services" class="services">
    <div class="services-grid">
      <div v-for="(service, index) in services" :key="index"
           :class="['service-card', service.type]">
        <div v-if="service.type === 'text'" class="service-text">
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
        </div>
        <div v-else class="service-image">
          <div class="image-placeholder">
            <IconTools :size="60" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { IconTools } from '@tabler/icons-vue'

const services = [
  {
    type: 'text',
    title: 'MECHANICAL POWERTRAIN DIAGNOSTICS/REPAIR',
    description: 'We service all parts of Volvo, Cummins, Detroit Diesel, and Paccar engine ranging from injectors, camshafts, valve adjustments, oil/coolant/air leaks, EGR/oil coolers, turbos, pumps, solenoids, radiators, etc… We service complete aftertreatment systems, such as filters, Oneboxes, DEF pumps, dosers, heater lines, etc… Support for transmission repairs also include clutches, actuators, bearings, solenoids, and sensors.'
  },
  {
    type: 'image'
  },
  {
    type: 'text',
    title: 'ELECTRICAL DIAGNOSTICS/REPAIR',
    description: 'We service the complete ABS system, radar cruise control components, lighting, engine electrical system, complete interior cabin electrical system, module repair, camera/ELD installations, and custom customer specified modifications. DEF/DPF system electrical harness and components are also support. We provide replacement harnesses, testing, and diagnostics. We repair trailer ABS systems as well!'
  },
  {
    type: 'image'
  },
  {
    type: 'image'
  },
  {
    type: 'text',
    title: 'CUSTOMER WIRING AND HARNESSES',
    description: 'We provide support for your custom projects: engine swaps, cab swaps, custom lighting, custom attachments, etc.. All inquires will need to be called in.'
  },
  {
    type: 'image'
  },
  {
    type: 'text',
    title: 'Tune up, preventative maintenance (PM) services',
    description: '• Full PM service – fuel filters, oil+filters, coolant, brakes adjustment, grease, air filters\n• Air conditioning- freon recovery/recharging, leak inspection, system diagnostics, component replacement\n• Pre purchase inspections- bring your truck to check for engine/transmission codes, find future problems, verify truck specs, etc…\n• We offer DOT annual inspections'
  }
]
</script>

<style lang="scss" scoped>
$primary-dark: #003D7A;
$primary-darker: #001F3F;
$gray-light: #f5f5f5;
$gray-medium: #ddd;
$gray-dark: #95a5a6;
$gray-darker: #7f8c8d;
$white: white;

.services {
  padding: 60px 0;
  background: $gray-light;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0;
  max-width: 100%;
}

.service-card {
  min-height: 350px;
  display: flex;
  align-items: center;
  justify-content: center;

  &.text {
    background: linear-gradient(135deg, $primary-dark 0%, $primary-darker 100%);
    color: $white;
    padding: 40px;
  }

  &.image {
    background: $gray-medium;
    overflow: hidden;
  }
}

.service-text {
  h3 {
    font-size: 20px;
    font-weight: 700;
    margin-bottom: 20px;
    line-height: 1.4;
    text-transform: uppercase;
  }

  p {
    font-size: 14px;
    line-height: 1.8;
    opacity: 0.95;
    white-space: pre-line;
  }
}

.image-placeholder {
  width: 100%;
  height: 100%;
  min-height: 350px;
  background: linear-gradient(135deg, $gray-dark 0%, $gray-darker 100%);
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgba(255, 255, 255, 0.3);
}

@media (max-width: 1024px) {
  .services-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .service-card {
    min-height: 300px;

    &.text {
      padding: 30px;
    }
  }

  .service-text h3 {
    font-size: 18px;
  }
}

@media (max-width: 768px) {
  .services {
    padding: 40px 0;
  }

  .services-grid {
    grid-template-columns: 1fr;
  }

  .service-card {
    min-height: 250px;

    &.text {
      padding: 25px;
    }
  }

  .service-text {
    h3 {
      font-size: 16px;
      margin-bottom: 15px;
    }

    p {
      font-size: 13px;
    }
  }
}
</style>
