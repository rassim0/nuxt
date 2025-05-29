<template>
  <div class="page-container">
  <section class="find-your-room">
    <div class="container">
      <h1 class="title">Find your room</h1>

      <div class="select-room">
        <p class="paragraph">
          Dining room, bedroom, bathroom or office. Find what you need
        </p>

        <div class="slider">
          <div
            class="slider-content"
            :style="{ transform: getSlideTransform() }"
              >








            <div class="slider-item">
              <div class="item-group">
                <div class="background">
                  <div class="mask">
                   <NuxtImg
  src="/bedroom.png"
  alt="Bedroom"
  aspect-ratio="597/773"
  width="100%"
  class="picture object-cover"
/>
                  </div>
                </div>
                <div class="content">
                  <span class="label">News arrivals</span>
                  <h2 class="item-title">Bedroom</h2>
                </div>
              </div>
            </div>









            <!-- Living room -->
            <div class="slider-item">
              <div class="item-group">
                <div class="background">
                  <div class="mask">
                    <NuxtImg
                      src="/Background.png"
                      alt="Living room"
                      class="picture"
                    />
                  </div>
             </div>
                <div class="content">
                  <span class="label">News arrivals</span>
                  <h2 class="item-title">Living room</h2>
                </div>
              </div>
            </div>





            <div class="slider-item">
              <div class="item-group">
                <div class="background">
                  <div class="mask">
                  <NuxtImg            
                  src="/Dining-room.jpg"
                      alt="Dining room"
                  class="picture"
                 />
                  </div>
                </div>
                <div class="content">
                  <span class="label">News arrivals</span>
                  <h2 class="item-title">Dining room</h2>
                </div>
              </div>
            </div>





  
           <div class="slider-item">
  <div class="item-group">
    <div class="background">
      <div class="mask">
        <NuxtImg
          src="/Bathroom.jpg"
          alt="Bathroom"
          class="picture"
          width="800"
          aspect-ratio="16/9"
        />
      </div>
    </div>
    <div class="content">
      <span class="label">News arrivals</span>
      <h2 class="item-title">Bathroom</h2>
    </div>
  </div>
</div>

  



            <div class="slider-item">
              <div class="item-group">
                <div class="background">
                  <div class="mask">
                    <NuxtImg
                      src="/Office.jpg"
                      alt="Office"
                      class="picture"
                    />
                  </div>
                </div>
                <div class="content">
                  <span class="label">News arrivals</span>
                  <h2 class="item-title" style="margin-left: 70px;">Office</h2>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="slider-nav">
        <div class="dots">
          {{ String(currentSlide + 1).padStart(2, "0") }} /
          {{ String(totalSlides).padStart(2, "0") }}
        </div>
        <div class="nav">
          <button @click="nextSlide" class="next">
            Next
            <svg width="9" height="16" viewBox="0 0 9 16" fill="none">
              <path d="M1 1L8 8L1 15" stroke="#A06056" stroke-width="2" />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const currentSlide = ref(0)
const totalSlides = 5
const slideWidth = 458.25
const slideGap = 32

const nextSlide = () => {
  currentSlide.value = (currentSlide.value + 1) % totalSlides
}

const getSlideTransform = () => {
  return `translateX(-${currentSlide.value * (slideWidth + slideGap)}px)`
}
</script>

<style scoped>


.page-container {
  display: flex;
  justify-content: center;
  width: 100%;
}


.find-your-room {
   background: #f3eee8;
  width: 1440px;
  height: 665px;
}

.container {
  width: 100%;
  max-width: 1440px;
  padding-right: 150px;
  padding-left: 150px;
  padding-top: 64px;
  padding-bottom: 70px ;
  box-sizing: border-box;
  gap: 48px;
}

.title {
  width: 1140px;
  height: 60px;
  font-family: "Merriweather", serif;
  font-style: normal;
  font-weight: 400;
  font-size: 55px;
  line-height: 60px;
  letter-spacing: -0.6px;
  color: #706458;
  margin: 0 0 48px 0;
}

.select-room {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 0;
  gap: 24px;
  width: 1140px;
  height: 350px;
  margin-bottom: 48px;
}

.paragraph {
  width: 165px;
  height: 100px;
  font-family: "Varta", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 25px;
  color: rgba(112, 100, 88, 0.9);
  letter-spacing: 0px;
  margin: 0;
}

.slider {
  width: 947.5px;
  height: 350px;
  overflow: hidden;
  position: relative;
}

.slider-content {
  display: flex;
  gap: 32px;
  transition: transform 0.3s ease-in-out;
  position: absolute;
}

.slider-item {
  width: 458.25px;
  height: 350px;
  flex-shrink: 0;
}

.item-group {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 0;
  gap: 32px;
  position: relative;
  width: 458.25px;
  height: 350px;
}

.background {
  width: 570.25px;
  height: 350px;
  position: relative;
}

.mask {
  position: absolute;
  left: 0%;
  right: 42.99%;
  top: 0%;
  bottom: 0%;
  background: #F3EEE8;
  border-radius: 1px;
  overflow: hidden;
}

.picture {

  width:597px;
  height: 773px;
  top: -423px;
  left: -254.3px;
  object-fit: cover;
}

.content {
  position: absolute;
  left: calc(261.25px + 32px);
  top: 0;
}

.label {
  display: block;
  width: 165px;
  height: 25px;
  font-family: "Varta", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 25px;
  color: rgba(112, 100, 88, 0.9);
  margin-bottom: 0px;
  margin-top: 20px;
}

.item-title {
  position: absolute;
  height: 430px;
  left: -99.27%;
  right: 52.93%;
  top: calc(200% - 330px / 2);
  font-family: "Merriweather";
  font-style: normal;
  font-weight: 400;
  font-size: 55px;
  line-height: 60px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: -0.6px;
  color: #a06056;
}

.slider-nav {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 0;
  gap: 30px;
  width: 1140px;
  height: 25px;
}

.dots {
  width: 165px;
  height: 25px;
  font-family: "Varta", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 25px;
  color: rgba(112, 100, 88, 0.9);
  opacity: 0.5;
}

.nav {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0;
  gap: 16px;
  width: 945px;
  height: 25px;
}

.next {
  display: flex;
  align-items: center;
  gap: 16px;
  font-family: "Karla", sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 25px;
  letter-spacing: 0.3px;
  color: #a06056;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
}

@media (max-width: 1440px) {
  .find-your-room {
    width: 100%;
    height: auto;
    padding: 32px 0;
  }

  .container {
    padding: 0 5%;
  }

  .title,
  .select-room,
  .slider-nav {
    width: 100%;
  }

  .slider {
    width: calc(100% - 165px - 24px);
  }

  .slider-item {
    width: calc(50% - 16px);
  }

  .item-group {
    width: 100%;
  }

  .background {
    width: 60%;
  }
}

@media (max-width: 768px) {
  .find-your-room {
    overflow: hidden;
  }

  .container {
    padding: 0 20px;
  }

  .title {
    font-size: 40px;
    line-height: 45px;
    margin-bottom: 24px;
  }

  .select-room {
    flex-direction: column;
    height: auto;
    gap: 24px;
  }

  .paragraph {
    width: 100%;
    height: auto;
    margin-bottom: 20px;
  }

  .slider {
    width: 100%;
    overflow: visible;
  }

  .slider-content {
    width: max-content;
  }

  .slider-item {
    width: 458.25px;
  }

  .item-group {
    width: 458.25px;
    overflow: visible;
  }

  .background {
    width: 458.25px;
  }

  .mask {
    right: 0;
    width: 100%;
  }

  .picture {
    width: 200.25px;
  }

  .content {
    left: 20px;
    bottom: -60px;
  }

  .label {
    top: -400px;
    margin-left: 200px;
  }

  .item-title {
    top: -300px;
    left: 120px;
    height: auto;
    font-size: 40px;
    line-height: 45px;
    text-align: left;
  }

  .slider-nav {
    margin-top: 80px;
  }

  .nav {
    width: calc(100% - 195px);
  }
}
</style>
