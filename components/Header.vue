<template>
  <div class="page-container">
    <!-- Combined Layout -->
    <div class="combined-section">
      <!-- Navbar (centered 1239.14px width) -->
      <div class="navbar-container">
        <div class="navbar">
          <NuxtLink to="/" class="logo">antic</NuxtLink>
          <div class="nav-links">
            <NuxtLink 
              v-for="link in navLinks" 
              :key="link.text" 
              :to="link.url" 
              class="nav-link"
            >
              {{ link.text }}
            </NuxtLink>
          </div>
        </div>
        <button class="contact-button">
          <img src="/Contact.svg" alt="">
        </button>
      </div>

      <!-- Left Column (720px) -->
      <div class="left-column">
        <!-- Hero Content - Updated to 420px width and 372px height -->
        <div class="hero-content">
          <span class="mini-title">HOME DESIGN</span>
          <h1 class="main-heading">Elegance for Interiors & Exteriors</h1>
          <p class="subtitle">
            We provide everyone with modern,<br> trendy, quality furniture
          </p>
          <button class="action-button">
            <img src="/Down.svg" alt="">
          </button>
        </div>
      </div>

      <!-- Right Column (720px) -->
      <div class="right-column">
        <NuxtImg 
          src="/jean-philippe-delberghe-Ry9WBo3qmoc-unsplash.jpg"
          alt="Interior design"
          class="hero-image"
          width="720"
          height="900"
          loading="eager"
          format="webp"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
const navLinks = [
  { text: 'Products', url: '/products' },
  { text: 'Rooms', url: '/rooms' },
  { text: 'Services', url: '/services' },
  { text: 'Inspirations', url: '/inspirations' }
]
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Merriweather:wght@300;700&family=Varta:wght@400;700&display=swap');

/* Base Layout */
.page-container {
  width: 1440px;
  height: 900px;
  margin: 0 auto;
  position: relative;
}

.combined-section {
  display: flex;
  height: 100%;
}

/* Navbar (1239.14px centered) */
.navbar-container {
  position: absolute;
  width: 1239.1353759765625px;
  height: 50px;
  justify-content: space-between;
  top: 55px;
  left: 149.9px;
  display: flex;
  z-index: 100;
}

.navbar {
  display: flex;
  width: 470px;
  height: 29px;
}

.nav-links {
  width: 344px;
  height: 25px;
  display: flex;
  gap: 24px;
  margin-right: auto;
  top: 14.5px;
  left: 126px;
  padding-top: 5px;
}

/* Left Column (720px) */
.left-column {
  width: 720px;
  height: 900px;
  gap: 48px;
  padding: 24px 150px;
  background-color:#F3EEE8;
  display: flex;
  align-items: center;
}

.logo {
  font-family: 'Merriweather', serif;
  font-weight: 700;
  font-size: 34px;
  line-height: 25px;
  letter-spacing: 2px;
  color: #a06056;
  width: 94px;
  height: 25px;
  top: 10.5px;
  margin-right: 32px;
}

.nav-link {
  font-family: 'Varta', sans-serif;
  font-weight: 400;
  font-size: 16px;
  color: #706458;
  white-space: nowrap;
  transition: color 0.3s ease; 
}

.nav-link:hover {
  color: #a06056;
}

.nav-link.router-link-exact-active {
  color: #a06056;
  font-weight: 700;
}

/* Updated Hero Content */
.hero-content {
  width: 420px;
  height: 372px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.mini-title {
  font-family: 'Varta', sans-serif;
  font-weight: 700;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 1px;
  color: #A06056;
  text-transform: uppercase;
  margin-bottom: 50px;
}

.main-heading {
  font-family: 'Merriweather', serif;
  font-weight: 300;
  font-size: 50px;
  line-height: 70px;
  letter-spacing: -0.4px;
  color: #a06056;
  margin-bottom: 30px;
}

.subtitle {
  font-family: 'varta', serif;
  font-weight: 400;
  font-size: 22px;
  line-height: 30.8px;
  letter-spacing: 0px;
  color: #706458;
  background: #F3EEE8;
  margin-bottom: 48px;
  width: 420px;
  height: 62px;
}

.action-button {
  width: 50px;
  height: 50px;
  border-radius: 100px;
  border: 2px solid #a06056;
  background: transparent;
  padding-left: 17px; 
  padding-right: 17px; 
  padding-top: 20px; 
  padding-bottom: 20px; 
  gap: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.3s ease;
}

.icon {
  width:16px ;
  height: 9px;
}


.action-button:hover {
  background-color: #ffffff;
}

/* Right Column (720px) */
.right-column {
  width: 720px;
  height: 900px;
  position: relative;
}

.contact-button {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255,255,255,0.2);
  backdrop-filter: blur(5px);
  border: none;
  cursor: pointer;
  transition: background 0.3s ease;
}

.contact-button:hover {
  background: rgba(255,255,255,0.3);
}

.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Responsive */
@media (max-width: 1024px) {
  .page-container {
    width: 100%;
    height: auto;
  }
  
  .combined-section {
    flex-direction: column;
  }
  
  .navbar-container {
    position: relative;
    top: 0;
    padding: 20px;
  }
  
  .navbar {
    width: 100%;
  }
  
  .left-column,
  .right-column {
    width: 100%;
    height: auto;
    aspect-ratio: 1;
    padding: 30px;
  }
  
  .left-column {
    padding-top: 30px;
  }

  .hero-content {
    width: 100%;
    height: auto;
    padding: 40px 0;
  }
}
</style>
