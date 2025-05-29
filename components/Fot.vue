<template>
  <footer class="footer">
    <div class="content">
      <!-- Logo and Navigation -->
      <nav class="navigation">
        <div class="logotype">antic</div>

        <div class="nav-sections">

         <!-- Products -->
          <div class="nav-section">
            <h3 class="nav-title">Products</h3>
            <div class="nav-links">
              <a href="#" class="nav-link">Furniture</a>
              <a href="#" class="nav-link">Decoration</a>
              <a href="#" class="nav-link">Storage</a>
              <a href="#" class="nav-link">Baby and child</a>
              <a href="#" class="nav-link">Connected home</a>
            </div>
          </div>


            <!-- Rooms -->
          <div class="nav-section">
            <h3 class="nav-title">Rooms</h3>
            <div class="nav-links">
              <a href="#" class="nav-link">Living room</a>
              <a href="#" class="nav-link">Dining room</a>
              <a href="#" class="nav-link">Cooked</a>
              <a href="#" class="nav-link">Bedroom</a>
              <a href="#" class="nav-link">Bathroom</a>
              <a href="#" class="nav-link">Office</a>
              <a href="#" class="nav-link">Laundry</a>
              <a href="#" class="nav-link">Garage</a>
            </div>
          </div>


          <!-- Services -->
          <div class="nav-section">
            <h3 class="nav-title">Services</h3>
            <div class="nav-links">
              <a href="#" class="nav-link">Click and collect</a>
              <a href="#" class="nav-link">Conception</a>
              <a href="#" class="nav-link">Installation</a>
              <a href="#" class="nav-link">Advices</a>
              <a href="#" class="nav-link">Gift card</a>
            </div>
          </div>


          <!-- About -->
          <div class="nav-section">
            <h3 class="nav-title">About</h3>
            <div class="nav-links">
              <a href="#" class="nav-link">Our story</a>
              <a href="#" class="nav-link">Our stores</a>
              <a href="#" class="nav-link">Our partners</a>
            </div>
          </div>

          <!-- Planet -->
          <div class="nav-section">
            <div class="planet-content">
              <h3 class="nav-title">We respect our planet</h3>
              <img src="/footer.png" alt="Interior design" class="planet-image" />
              <p class="planet-text">
                We're taking positive steps to reduce our impact on the planet. For us, that means retailing responsibly.
              </p>
              <a href="#" class="learn-more">Learn more <Icon name="ep:arrow-right" style="color:#a06056; " /></a>
            </div>
          </div>
        </div>
      </nav>
<div class="copy">
      <!-- Social Icons -->
      <div class="social-networks">
        <a href="#" class="social-icon"><img src="/Facebook.svg" alt="Facebook"></a>
        <a href="#" class="social-icon"><img src="/Twitter.svg" alt="Twitter"></a>
        <a href="#" class="social-icon"><img src="/Linkedin.svg" alt="LinkedIn"></a>
        <a href="#" class="social-icon"><img src="/Instagram.svg" alt="Instagram"></a>
      </div>

      <!-- Footer -->
      <div class="footer-bottom">
        <span class="copyright">© 2021 Agence Dnd</span>
        <div class="footer-links">
          <a href="#" class="footer-link">Privacy policy</a>
          <a href="#" class="footer-link">Term of service</a>
          <a href="#" class="footer-link">Language</a>
        </div>
      </div>
  </div>
 </div>

  </footer>
</template>

<style scoped>
.footer {
  background: #F3EEE8;
  width: 1440px;
  height: 628px;
  margin: 0 auto;
}

.content {
  max-width: 1440px;
  margin: 0 auto;

}

.navigation {
  display: flex;
  width: 1140px;
  height: 396px;
  gap: 64px;
  padding-top: 70px;
  padding-right: 150px;
  padding-bottom: 64px;
  padding-left:150px;
}

.logotype {
  font-family: 'Merriweather';
  font-weight: 700;
  font-size: 34px;
  line-height: 25px;
  letter-spacing: 2px;
  color: #534B42;
  width: 94px;
  height: 25px;
}

.nav-sections {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  gap: 48px;
  width: 683px;
  height: 336px;
  flex: 1;
}

.nav-section{
  width: 134.75px;
  height: 30px;
  gap: 22px;

}

.nav-title {
  font-family: 'Varta';
  font-weight: 600;
  font-size: 25px;
  line-height: 30px;
  letter-spacing: -0.2px;
  color: #534B42;
  margin-bottom: 22px;
}

.nav-links {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.nav-link {
  font-family: 'Varta';
  font-size: 18px;
   font-weight: 400;
  line-height: 25px;
  letter-spacing: 0px;
  color: #706458;
  text-decoration: none;
}

.planet-image {
  width: 100%;
  height: 160px;
  object-fit: cover;
 margin-bottom: 15px;
}


.planet-content{
  width: 235px;
  height: 100px;
  gap: 24px;
}

.planet-text {
  font-family: 'Varta';
  font-weight: 400;
  font-size: 16px;
  line-height: 25px;
  letter-spacing: 0px;
  color: #706458;
  margin-bottom: 15px;
}

.learn-more {
  font-family: 'Karla';
  font-weight: 700;
  font-size: 17px;
  line-height: 25px;
  letter-spacing: 0.3px;
  color: #A06056;

  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.social-networks {
  display: flex;
  justify-content: center;
  gap: 24px;
 margin-top: 78px;
}

.social-icon {
  width: 32px;
  height: 32px;
}

.footer-bottom {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.copyright {
  font-family: 'Varta';
  font-size: 18px;
  color: rgba(112, 100, 88, 0.7);
}

.footer-links {
  display: flex;
  gap: 30px;
}

.footer-link {
  font-family: 'Varta';
  font-size: 18px;
  color: rgba(112, 100, 88, 0.7);
  text-decoration: none;
}
.copy{
  width: 1140px;
  height: 77px;
  margin: 48px auto;
}

@media (max-width: 1024px) {
  .footer {
    padding: 40px 40px 20px;
  }
  
  .navigation {
    flex-direction: column;
    gap: 40px;
  }

  .nav-sections {
    display: flex;
    flex-direction: column;
    gap: 40px;
  }
  .nav-section {
    width: 100%;
  }

  .planet-image,
  .planet-text {
    max-width: 400px;
  }

  .social-networks {
    justify-content: flex-start;
  }

  .footer-bottom {
    padding-top: 20px;
  }
}

@media (max-width: 640px) {
  .footer-bottom {
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
  }

  .footer-links {
    flex-direction: column;
    gap: 12px;
  }
}
</style>
