<template>
  <header class="top-bar">
    <div class="container">
      <div class="top-bar-content">
        <div class="contact-info">
          <div class="info-item">
            <IconPhone/>
            <span>Call us: (440)829-2132</span>
          </div>
          <div class="info-item">
            <IconClock/>
            <span>Opening hours: Mon - Fri: 9.00am - 5.00pm</span>
          </div>
        </div>
        <div class="social-links">
          <a href="https://www.instagram.com" target="_blank" aria-label="Instagram">
            <IconBrandInstagram/>
          </a>
          <a href="tel:4408292132" aria-label="Phone">
            <IconPhone/>
          </a>
        </div>
      </div>
    </div>
  </header>

  <header class="main-nav">
    <div class="container">
      <div class="nav-content">
        <div class="logo">
          <span class="logo-text">FLEETWORKS</span>
        </div>

        <button class="mobile-menu-toggle" @click="toggleMobileMenu" aria-label="Toggle menu">
          <IconMenu2 v-if="!mobileMenuOpen" :size="24"/>
          <IconX v-else :size="24"/>
        </button>

        <ul class="nav-menu" :class="{ 'active': mobileMenuOpen }">
          <li><a href="#home" @click="closeMobileMenu">Home</a></li>
          <li><a href="#services" @click="closeMobileMenu">Services</a></li>
          <li><a href="#aboutus" @click="closeMobileMenu">About Us</a></li>
          <li><a href="#contacts" @click="closeMobileMenu">Contacts</a></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script setup>
import {ref} from 'vue'
import {IconPhone, IconClock, IconBrandInstagram, IconMenu2, IconX} from '@tabler/icons-vue'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}

const closeMobileMenu = () => {
  mobileMenuOpen.value = false
}
</script>

<style lang="scss" scoped>
$primary-color: #002D5B;
$accent-color: #E74C3C;
$text-color: #333;
$border-color: #eee;
$white: white;

header {
  background: $white;
}

.top-bar {
  background: $primary-color;
  color: $white;
  padding: 10px 0;
  font-size: 14px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

.top-bar-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.contact-info {
  display: flex;
  gap: 30px;
}

.info-item {
  display: flex;
  align-items: center;
  gap: 8px;
}

.social-links {
  display: flex;
  gap: 15px;

  a {
    color: $white;
    text-decoration: none;
    transition: opacity 0.3s;
    display: flex;
    align-items: center;

    &:hover {
      opacity: 0.8;
    }
  }
}

.main-nav {
  position: sticky;
  top: 0;
  z-index: 1000;

  background: $white;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  padding: 15px 0;
}

.nav-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-text {
  font-size: 28px;
  font-weight: 700;
  color: $primary-color;
  letter-spacing: 1px;
}

.mobile-menu-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 5px;
  color: $primary-color;
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 30px;

  li a {
    text-decoration: none;
    color: $text-color;
    font-weight: 500;
    font-size: 16px;
    transition: color 0.3s;
    padding: 8px 15px;

    &:hover {
      color: $accent-color;
    }
  }
}

@media (max-width: 768px) {
  .top-bar {
    font-size: 12px;
    padding: 8px 0;
  }

  .top-bar-content {
    flex-direction: column;
    gap: 10px;
    text-align: center;
  }

  .contact-info {
    flex-direction: column;
    gap: 8px;
  }

  .info-item {
    justify-content: center;
    font-size: 12px;
  }

  .mobile-menu-toggle {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .nav-menu {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: $white;
    flex-direction: column;
    gap: 0;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);

    &.active {
      max-height: 300px;
    }

    li {
      border-bottom: 1px solid $border-color;

      a {
        display: block;
        padding: 15px 20px;
      }
    }
  }

  .logo-text {
    font-size: 22px;
  }
}

@media (max-width: 480px) {
  .top-bar {
    font-size: 11px;
  }

  .logo-text {
    font-size: 20px;
  }
}
</style>
