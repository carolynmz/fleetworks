<template>
  <section id="contacts" class="contact">
    <div class="contact-header">
      <h2>Contact Us</h2>
    </div>

    <div id="scheduleservice" class="contact-content">
      <div class="container">
        <div class="contact-grid">
          <div class="office-info">
            <h2>Our Office</h2>
            <div class="divider"></div>

            <div class="info-block">
              <IconMapPin :size="24" class="icon-svg"/>
              <div class="info-text">
                <h5>Address</h5>
                <p>3024 Brecksville Rd Ste B Richfield, Ohio 44286</p>
              </div>
            </div>

            <div class="info-block">
              <IconPhone :size="24" class="icon-svg"/>
              <div class="info-text">
                <h5>Phone</h5>
                <p>(440)829-2132</p>
              </div>
            </div>

            <div class="info-block">
              <IconMail :size="24" class="icon-svg"/>
              <div class="info-text">
                <h5>Email</h5>
                <p>fleetworksmain@gmail.com</p>
              </div>
            </div>

            <div class="info-block">
              <IconBuildingWarehouse :size="24" class="icon-svg"/>
              <div class="info-text">
                <h5>Opening Hours</h5>
                <p>Mon - Fri: 9.00am to 5.00pm</p>
              </div>
            </div>
          </div>

          <div class="office-image">
            <img class="image" src="/images/top-view.webp" alt="">
          </div>

          <div class="contact-form-wrapper">
            <h3>Schedule service</h3>
            <form @submit.prevent="handleSubmit" class="contact-form">
              <div class="form-group">
                <label for="name">Your name</label>
                <input type="text" id="name" v-model="formData.name" required>
              </div>

              <div class="form-group">
                <label for="company">Company Name</label>
                <input type="text" id="company" v-model="formData.company">
              </div>

              <div class="form-group">
                <label for="phone">Phone number</label>
                <input type="tel" id="phone" v-model="formData.phone">
              </div>

              <div class="form-group">
                <label for="truck">Truck year make & model</label>
                <input type="text" id="truck" v-model="formData.truck">
              </div>

              <div class="form-group">
                <label for="description">Description</label>
                <textarea id="description" v-model="formData.description" rows="5"></textarea>
              </div>

              <button type="submit" class="submit-btn">SEND NOW</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import {ref} from 'vue'
import {IconMapPin, IconPhone, IconMail, IconBuildingWarehouse} from '@tabler/icons-vue'

const formData = ref({
  name: '',
  company: '',
  phone: '',
  truck: '',
  description: ''
})

const handleSubmit = () => {
  alert('Form submitted! (This is a demo - no actual submission)')
  console.log('Form data:', formData.value)
}
</script>

<style lang="scss" scoped>
$primary-color: #002D5B;
$accent-color: #E74C3C;
$accent-dark: #C0392B;
$gray-light: #f5f5f5;
$gray-medium: #ddd;
$gray-dark: #555;
$gray-darker: #7f8c8d;
$gray-darkest: #95a5a6;
$white: white;

.contact {
  background: $white;
}

.contact-header {
  background: linear-gradient(rgba($primary-color, 0.9), rgba($primary-color, 0.9)),
  url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 200"><rect fill="%23333" width="1200" height="200"/></svg>');
  background-size: cover;
  background-position: center;
  padding: 60px 20px;
  text-align: center;
  color: $white;

  h2 {
    font-size: 42px;
    font-weight: 700;
    text-transform: uppercase;
  }
}

.contact-content {
  padding: 60px 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 40px;
}

.office-info {
  h2 {
    font-size: 32px;
    font-weight: 700;
    color: $primary-color;
    margin-bottom: 20px;
  }
}

.divider {
  width: 60px;
  height: 3px;
  background: $accent-color;
  margin-bottom: 30px;
}

.info-block {
  display: flex;
  gap: 15px;
  margin-bottom: 25px;
  align-items: flex-start;
}

.icon-svg {
  color: $accent-color;
  flex-shrink: 0;
  margin-top: 2px;
}

.info-text {
  h5 {
    font-size: 16px;
    font-weight: 700;
    color: $primary-color;
    margin-bottom: 5px;
  }

  p {
    font-size: 14px;
    color: $gray-dark;
    line-height: 1.6;
  }
}

.office-image {
  display: flex;
  align-items: center;
  justify-content: center;
}

.image {
  width: 100%;
  //height: 500px;
  background: linear-gradient(135deg, $gray-darkest 0%, $gray-darker 100%);
  border-radius: 8px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;

  .placeholder-icon {
    opacity: 0.3;
    color: $white;
  }
}

.contact-form-wrapper {
  background: $primary-color;
  padding: 35px;
  border-radius: 8px;
  color: $white;

  h3 {
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 25px;
  }
}

.contact-form {
  .form-group {
    margin-bottom: 20px;
  }

  label {
    display: block;
    font-size: 14px;
    margin-bottom: 8px;
    font-weight: 500;
  }

  input,
  textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid $gray-medium;
    border-radius: 4px;
    font-size: 14px;
    font-family: inherit;
    transition: border-color 0.3s;

    &:focus {
      outline: none;
      border-color: $accent-color;
    }
  }

  textarea {
    resize: vertical;
  }
}

.submit-btn {
  width: 100%;
  padding: 14px;
  background: $accent-color;
  color: $white;
  border: none;
  border-radius: 4px;
  font-size: 15px;
  font-weight: 700;
  cursor: pointer;
  transition: background 0.3s;
  letter-spacing: 1px;

  &:hover {
    background: $accent-dark;
  }
}

@media (max-width: 1024px) {
  .contact-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .office-image {
    order: 2;
  }

  .contact-form-wrapper {
    order: 3;
  }

  .image {
    width: auto;
    max-height: 400px;
  }
}

@media (max-width: 768px) {
  .contact-header {
    padding: 40px 20px;

    h2 {
      font-size: 32px;
    }
  }

  .contact-content {
    padding: 40px 0;
  }

  .office-info h2 {
    font-size: 26px;
  }

  .contact-form-wrapper {
    padding: 25px;

    h3 {
      font-size: 20px;
    }
  }
}

@media (max-width: 480px) {
  .contact-header h2 {
    font-size: 26px;
  }

  .info-block {
    flex-direction: column;
    gap: 8px;
  }
}
</style>
