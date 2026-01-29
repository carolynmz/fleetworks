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
              <div class="icon">📍</div>
              <div class="info-text">
                <h5>Address</h5>
                <p>3024 Brecksville Rd Ste B Richfield, Ohio 44286</p>
              </div>
            </div>

            <div class="info-block">
              <div class="icon">📞</div>
              <div class="info-text">
                <h5>Phone</h5>
                <p>(440)829-2132</p>
              </div>
            </div>

            <div class="info-block">
              <div class="icon">✉️</div>
              <div class="info-text">
                <h5>Email</h5>
                <p>fleetworksmain@gmail.com</p>
              </div>
            </div>

            <div class="info-block">
              <div class="icon">🏢</div>
              <div class="info-text">
                <h5>Opening Hours</h5>
                <p>Mon - Fri: 9.00am to 5.00pm</p>
              </div>
            </div>
          </div>

          <div class="office-image">
            <div class="image-placeholder"></div>
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
import { ref } from 'vue'

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

<style scoped>
.contact {
  background: white;
}

.contact-header {
  background: linear-gradient(rgba(0, 45, 91, 0.9), rgba(0, 45, 91, 0.9)),
              url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 200"><rect fill="%23333" width="1200" height="200"/></svg>');
  background-size: cover;
  background-position: center;
  padding: 60px 20px;
  text-align: center;
  color: white;
}

.contact-header h2 {
  font-size: 42px;
  font-weight: 700;
  text-transform: uppercase;
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

.office-info h2 {
  font-size: 32px;
  font-weight: 700;
  color: #002D5B;
  margin-bottom: 20px;
}

.divider {
  width: 60px;
  height: 3px;
  background: #E74C3C;
  margin-bottom: 30px;
}

.info-block {
  display: flex;
  gap: 15px;
  margin-bottom: 25px;
}

.info-block .icon {
  font-size: 24px;
  color: #E74C3C;
}

.info-text h5 {
  font-size: 16px;
  font-weight: 700;
  color: #002D5B;
  margin-bottom: 5px;
}

.info-text p {
  font-size: 14px;
  color: #555;
  line-height: 1.6;
}

.office-image {
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-placeholder {
  width: 100%;
  height: 500px;
  background: linear-gradient(135deg, #95a5a6 0%, #7f8c8d 100%);
  border-radius: 8px;
  position: relative;
}

.image-placeholder::after {
  content: '🏢';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 80px;
  opacity: 0.3;
}

.contact-form-wrapper {
  background: #002D5B;
  padding: 35px;
  border-radius: 8px;
  color: white;
}

.contact-form-wrapper h3 {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 25px;
}

.contact-form .form-group {
  margin-bottom: 20px;
}

.contact-form label {
  display: block;
  font-size: 14px;
  margin-bottom: 8px;
  font-weight: 500;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 4px;
  font-size: 14px;
  font-family: inherit;
  transition: border-color 0.3s;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none;
  border-color: #E74C3C;
}

.contact-form textarea {
  resize: vertical;
}

.submit-btn {
  width: 100%;
  padding: 14px;
  background: #E74C3C;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 15px;
  font-weight: 700;
  cursor: pointer;
  transition: background 0.3s;
  letter-spacing: 1px;
}

.submit-btn:hover {
  background: #C0392B;
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

  .image-placeholder {
    max-height: 400px;
  }
}

@media (max-width: 768px) {
  .contact-header {
    padding: 40px 20px;
  }

  .contact-header h2 {
    font-size: 32px;
  }

  .contact-content {
    padding: 40px 0;
  }

  .office-info h2 {
    font-size: 26px;
  }

  .contact-form-wrapper {
    padding: 25px;
  }

  .contact-form-wrapper h3 {
    font-size: 20px;
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

  .image-placeholder {
    height: 300px;
  }
}
</style>
