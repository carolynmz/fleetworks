<template>
  <section class="map-section">
    <div class="map-container">
      <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3003.8282!2d-81.6406!3d41.2369!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDHCsDE0JzEyLjgiTiA4McKwMzgnMjYuMiJX!5e0!3m2!1sen!2sus!4v1234567890"
          width="100%"
          height="450"
          style="border:0;"
          allowfullscreen
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          title="3024 Brecksville Rd Ste B Richfield, Ohio 44286"
      ></iframe>
    </div>
  </section>
</template>

<style lang="scss" scoped>
$gray-light: #f5f5f5;

.map-section {
  background: $gray-light;
}

.map-container {
  width: 100%;
  height: 450px;

  iframe {
    display: block;
    width: 100%;
    height: 100%;
  }
}

@media (max-width: 768px) {
  .map-container {
    height: 350px;
  }
}

@media (max-width: 480px) {
  .map-container {
    height: 300px;
  }
}
</style>
