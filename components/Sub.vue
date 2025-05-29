<template>
  <section class="trends-section">
    <div class="container">
      <div class="header">
        <div class="title-group">
          <h2 class="title">Be aware of the latest trends</h2>
          <p class="subtitle">
            Stay informed of new trends, but also of our various offers.
          </p>
          <a href="#" class="learn-more">Learn more <Icon name="ep:arrow-right" size="24px" /></a>
        </div>
        <div class="subscription">
          <input
            type="email"
            placeholder="email@address.com"
            class="email-input"
          />
          <button class="subscribe-btn">Subscribe</button>
        </div>
      </div>

      <div class="inspiration-section">
        <div class="carousel">
          <Swiper
             :slides-per-view="2.5"
             :space-between="30"
             @swiper="setSwiperInstance"
             @slideChange="onSlideChange" 
             class="carousel-content"
    :style="{ '--swiper-slide-width': '458px' }"
          >
            <!-- Slide 1 -->
            <SwiperSlide>
              <div class="carousel-item">
                <div class="image-container">
                  <NuxtImg
                    src="/jean-philippe-delberghe-feijc-nqWKM-unsplash.jpg"
                    alt="Chair"
                    width="458"
                    height="550"
                    format="webp"
                    placeholder
                    class="zoomed-image"
                  />
                </div>
              </div>
            </SwiperSlide>

            <!-- Slide 2 -->
            <SwiperSlide>
              <div class="carousel-item">
                <div class="image-container">
                  <NuxtImg
                    src="/jorge-de-jorge-pHbAY99SRB4-unsplash.jpg"
                    alt="Living room"
                    width="458"
                    height="550"
                    format="webp"
                    placeholder
                    class="zoomed-image"
                  />
                </div>
              </div>
            </SwiperSlide>

            <!-- Slide 3 -->
            <SwiperSlide>
              <div class="carousel-item">
                <div class="image-container">
                  <NuxtImg
                    src="/minh-pham-OtXADkUh3-I-unsplash.jpg"
                    alt="Tables"
                    width="458"
                    height="550"
                    format="webp"
                    placeholder
                    class="zoomed-image"
                  />
                </div>
              </div>
            </SwiperSlide>

            <!-- Slide 4 -->
            <SwiperSlide>
              <div class="carousel-item">
                <div class="image-container">
                  <NuxtImg
                    src="/Dining-room.jpg"
                    alt="Decoration"
                    width="458"
                    height="550"
                    format="webp"
                    placeholder
                    class="zoomed-image"
                  />
                </div>
              </div>
            </SwiperSlide>

            <!-- Slide 5 -->
            <SwiperSlide>
              <div class="carousel-item">
                <div class="image-container">
                  <NuxtImg
                    src="/bedroom.png"
                    alt="Bedroom"
                    width="458"
                    height="550"
                    format="webp"
                    placeholder
                    class="zoomed-image"
                  />
                </div>
              </div>
            </SwiperSlide>
          </Swiper>
        </div>
      </div>

      <div class="carousel-nav">
        <div class="inspiration-header">
          <h3 class="inspiration-title">Inspirations</h3>
          <p class="inspiration-text">
            Our experts are keen to stay on top of trends in order to offer
            you new inspirations for your interior and exterior every day.
            Remember that to inspire you we have to inspire ourselves and we
            want to share that with you.
          </p>
        </div>

        <div class="takeittop">
          <button
            @click="prevSlide"
            class="nav-btn prev"
            :disabled="currentSlide === 0"
          >
            <!-- Left Arrow SVG -->
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M15 18L9 12L15 6"
                stroke="#706458"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </button>

          <button
            @click="nextSlide"
            class="nav-btn next"
            :disabled="currentSlide === totalSlides - 1"
          >
            <!-- Right Arrow SVG -->
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M9 18L15 12L9 6"
                stroke="#706458"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </button>

           <div class="slide-counter">
    {{ String(currentSlide + 1).padStart(2, "0") }} / 
    {{ String(totalSlides).padStart(2, "0") }}
  </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'

const swiperInstance = ref(null)
const currentSlide = ref(0)
const totalSlides = 5

const setSwiperInstance = (swiper) => {
  swiperInstance.value = swiper
  // Sync initial index
  currentSlide.value = swiper.activeIndex
}

const nextSlide = () => {
  if (swiperInstance.value && !swiperInstance.value.isEnd) {
    swiperInstance.value.slideNext()
  }
}

const prevSlide = () => {
  if (swiperInstance.value && !swiperInstance.value.isBeginning) {
    swiperInstance.value.slidePrev()
  }
}

// Update currentSlide when Swiper changes
const onSlideChange = (swiper) => {
  currentSlide.value = swiper.activeIndex
}
</script>

<style scoped>
.trends-section {
  padding: 64px 150px;
  background: #ffffff;
  width: 100%;
  max-width: 1440px;
  height: 1034px;
  margin: 0 auto;
  box-sizing: border-box;
}

.container {
  max-width: 1144px;
  margin: 0 auto;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 1140.208251953125px;
  height: 115px;
  gap: 189px;
}

.title-group {
  width: 496px;
  height: 115px;
  gap: 10px;
}

.title {
  font-family: "Merriweather", serif;
  font-size: 35px;
  line-height: 40px;
  font-weight: 400;
  color: #121212;
  letter-spacing: -0.3px;
  width: 496px;
  height: 40px;
  margin-bottom: 15px;
}

.subtitle {
  font-family: "Varta", sans-serif;
  font-size: 18px;
  line-height: 25px;
  font-weight: 400;
  color: rgba(112, 100, 88, 0.9);
  letter-spacing: 0px;
  margin-bottom: 10px;
}

.learn-more {
  font-family: 'Karla';
  font-weight: 700;
  font-size: 17px;
  line-height: 25px;
  letter-spacing: 0.3px;
  color: #A06056;
  width: 120px;
  height: 25px;
  display: inline-flex; 
  align-items: center;
  gap: 6px;
}

.subscription {
  display: flex;
  gap: 16px;
  width: 455.21px;
  height: 50px;
}

.email-input {
  width: 296.1px;
  height: 50px;
  padding: 0 16px;
  border: none;
  background: #F3EEE8;
  font-family: "Varta", sans-serif;
  font-weight: 400;
  font-size: 18px;
  line-height: 25px;
  color: #706458;
}

.subscribe-btn {
  width: 143.11279296875px;
  height: 50px;
  padding-top: 8px;
  padding-right: 30px;
  padding-bottom: 8px;
  padding-left: 30px;
  gap: 10px;
  border-radius: 1px;
  font-weight: 700;
  font-size: 17px;
  line-height: 25px;
  letter-spacing: 0.3px;
  text-align: center;
  vertical-align: middle;
  background: #706458;
  color: #ffffff;
  border: none;
  font-family: "Karla", sans-serif;
  cursor: pointer;
}

.inspiration-section {
  width: 1440px;
  height: 550px;
  margin-top: 64px;
  gap: 30px;
}

.inspiration-header {
  width: 749px;
  height: 125px;
  display: flex;
  align-items: center;
  gap: 30px;
  margin-bottom: 0;
}

.inspiration-title {
  font-family: "Merriweather", serif;
  font-size: 45px;
  line-height: 40px;
  color: #534B42;
  font-weight: 300;
  letter-spacing: -0.3px;
  width: 360px;
  height: 40px;
  margin: 0;
}

.inspiration-text {
  font-family: "Varta", sans-serif;
  font-size: 18px;
  line-height: 25px;
  font-weight: 400;
  letter-spacing: 0px;
  color: rgba(112, 100, 88, 0.9);
  width: 359px;
  height: 125px;
  margin-top: 40px;
}

.takeittop {
  display: flex;
  align-items: center;
  gap: 20px;
  width: 165px;
  height: 85px;
}

.carousel {
  position: relative;
  overflow: visible;
  width: 1209px;
}

.carousel-content {
  display: flex;
  transition: transform 0.3s ease-in-out;
}

.carousel-item {
  width: 458px;
  margin-right: 32px;
}

.carousel-item:last-child {
  margin-right: 0;
}

.image-container {
  position: relative;
  overflow:hidden;
  padding-right: 0px;
}

.image-container img {
  width: 100%;
  height: 550px;
  object-fit: cover;
 padding-right: 0px;
}

.zoomed-image {
  transform: scale(1.2);
  transform-origin: center;
}

.label {
  font-family: "Varta", sans-serif;
  font-size: 18px;
  line-height: 2;
  color: #333;
}

.carousel-nav {
  display: flex;
  justify-content: space-between;
  align-items: flex-start; /* Align items to top */
  width: 100%;
  margin-top: 20px;
}

.nav-btn {
  width: 40px;
  height: 40px;
  background: none;
  border: 2px solid #706458; /* Circular border */
  border-radius: 50%; /* Circular shape */
  cursor: pointer;
  padding: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-btn:disabled {
  opacity: 0.5; /* Visible when disabled */
  cursor: not-allowed;
}

.slide-counter {
  font-family: "Varta", sans-serif;
  font-size: 16px;
  color: #706458;
  opacity: 0.8;
}

@media (max-width: 1440px) {
  .trends-section {
    padding: 48px 40px;
  }
  .container {
    width: 100%;
    height: auto;
    padding-top: 70px;
    padding-bottom: 70px;
  }
  .inspiration-section {
    width: 100%;
    padding-left: 0;
    margin-top: 32px;
  }
  .carousel {
    width: 100%;
  }
  .takeittop {
    position: static;
    margin-top: 10px;
  }
  .slide-counter {
    position: static;
  }
}

@media (max-width: 1024px) {
  .trends-section {
    padding: 48px 40px;
  }

  .header {
    flex-direction: column;
    gap: 20px;
  }

  .subscription {
    width: 100%;
  }
  .takeittop {
    display: none;
    visibility: hidden;
  }
  .carousel-item {
    width: calc(50% - 16px);
    min-width: unset;
  }
}

@media (max-width: 768px) {
  .trends-section {
    padding: 32px;
  }

  .title {
    font-size: 40px;
    line-height: 45px;
  }

  .inspiration-title {
    font-size: 25px;
    line-height: 45px;
    margin-bottom: 0px;
  }

  .inspiration-text {
    margin: 0 0 32px 0;
    max-width: 100%;
  }

  .carousel {
    overflow: visible;
  }

  .carousel-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    transform: none !important;
  }

  .carousel-item {
    min-width: unset;
    margin-right: 0;
    width: 100%;
  }

  .image-container {
    position: relative;
    width: 100%;
    overflow: hidden;
  }

  .image-container img {
    height: 200px;
    width: 100%;
    object-fit: cover;
  }

  .zoomed-image {
    transform: scale(1.2);
  }

  .takeittop {
    display: none;
    visibility: hidden;
  }

  .inspiration-section {
    margin-top: 32px;
  }

  .inspiration-header {
    margin-bottom: 24px;
  }

  .carousel-nav {
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    margin-bottom: 32px;
  }

  .slide-counter {
    display: none;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .carousel-content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }

  .carousel-item {
    min-width: unset;
    margin-right: 0;
  }

  .image-container img {
    height: 300px;
  }

  .zoomed-image {
    transform: scale(1.2);
  }
}
</style>