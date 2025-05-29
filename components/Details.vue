<template>
  <section class="design-services">
    <div class="container">
      <div class="left-column">
        <h2 class="main-title">We stay by your side to design your projects</h2>
        <a href="#" class="find-more">Find out more <Icon name="ep:arrow-right" style="color:#a06056; " /> </a>  
      </div>

      <div class="services-grid">
        <div class="service-card">
          <h3 class="service-title">Our Advices</h3>
          <p class="service-description">
            What if you took advantage of this rather special period to rethink
            your interior? You spend more time at home so you might as well feel
            good there.
          </p>
        </div>

        <div class="service-card">
          <h3 class="service-title">Click and Collect</h3>
          <p class="service-description">
            Adapted and contactless. Free from € 200 of purchases in stores
            offering the service.
          </p>
        </div>

        <div class="service-card">
          <h3 class="service-title">Conception Service</h3>
          <p class="service-description">
            Personalized service with an expert advisor for your interior and
            exterior decoration or layout projects.
          </p>
        </div>

        <div class="service-card">
          <h3 class="service-title">Installation Service</h3>
          <p class="service-description">
            Our furniture packaged in flat packs are designed for easy assembly.
            But you can call on our partner.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// No logic needed
</script>

<style scoped>
.design-services {
  display: flex;
  justify-content: center;
}

.container {
  background: #f3eee8;
  width: 1440px;
  height: 493px;
  gap: 48px;
  padding-top: 64px;
  padding-right: 150px;
  padding-bottom: 70px;
  padding-left: 150px;
  display: flex;
  flex-direction: row;
}

.left-column {
  flex: 0 0 380px;
  width: 546px;
  height: 243px;
  gap: 30px;

}

.main-title {
   width: 458px ;
   height : 188px; 
  font-family: "Merriweather", serif;
  font-size: 55px;
  line-height: 60px;
  letter-spacing :-0.6px ;
  color: #706458;
  font-weight: 400;
  margin-bottom: 30px;
}

.find-more {
  font-family: "Karla", serif;
  font-weight: 700;
  font-size: 17px;
  line-height: 25px;
  letter-spacing: 0.3px;
  color: #A06056;
 
  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.services-grid {
  display: grid;
  width : 546px;
  height : 359px;
  padding-top: 20px;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
  flex: 1;
}

.service-card {
  max-width: 258.5px;
}

.service-title {
  font-family: 'Varta';
  font-style: normal;
  font-weight: 600;
  font-size: 25px;
  line-height: 30px;
  letter-spacing: -0.2px;
  color: #A06056;
}

.service-description {
  font-family: "Varta", sans-serif;
  color: #666666;
  font-size: 18px;
  font-weight: 400;
  line-height:25px;
  letter-spacing: 0px ;
  margin-top: 12px;
}

@media (max-width: 1024px) {
  .container {
    flex-direction: column;
    padding: 0 24px;
  }

  .left-column {
    width: 100%;
    flex: none;
  }

  .main-title {
    font-size: 36px;
    margin-bottom: 24px;
  }

  .services-grid {
    grid-template-columns: 1fr;
    gap: 32px;
    width: 100%;
  }

  .service-card {
    max-width: 100%;
  }

  .service-title {
    font-size: 20px;
    margin-bottom: 12px;
  }
}
</style>
