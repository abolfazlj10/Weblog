<script>
  import { ref } from 'vue';
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

  import 'swiper/css/pagination';
  import 'swiper/css/navigation';

  // import required modules
  import { Autoplay, Pagination, Navigation } from 'swiper';

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const progressCircle = ref(null);
      const progressContent = ref(null);
      const onAutoplayTimeLeft = (s, time, progress) => {
        progressCircle.value.style.setProperty('--progress', 1 - progress);
        progressContent.value.textContent = `${Math.ceil(time / 1000)}s`;
      };
      return {
        onAutoplayTimeLeft,
        progressCircle,
        progressContent,
        modules: [Autoplay, Pagination, Navigation],
      };
    },
  };

</script>
<template>
    <swiper
    loop="true"
    speed="1000"
    :spaceBetween="30"
    :centeredSlides="true"
    :autoplay="{
      delay: 2500,
      disableOnInteraction: false,
    }"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    @autoplayTimeLeft="onAutoplayTimeLeft"
    class="mySwiper"
  >
    <swiper-slide class="SI" style="background-image:url('slide_4.jpg');"><div class="LI">slide 1</div></swiper-slide>
    <swiper-slide class="SI" style="background-image:url('photo_1_2023-06-14_12-33-11.jpg');"><div class="LI">slide 2</div></swiper-slide>
    <swiper-slide class="SI" style="background-image:url('photo_2023-06-14_12-49-30.jpg');"><div class="LI">slide 3</div></swiper-slide>
    <swiper-slide class="SI" style="background-image:url('d619a64645bf2cbf8f32f9063cf29ac5.jpg');"><div class="LI">slide 4</div></swiper-slide>
    
    <template #container-end>
      <div class="autoplay-progress">
        <svg viewBox="0 0 48 48" ref="progressCircle">
          <circle cx="24" cy="24" r="20"></circle>
        </svg>
        <span class="timer" ref="progressContent"></span>
      </div>
    </template>
  </swiper>
</template>
<style>

.swiper {
    height: 500px;
    width:100%;
    margin:10px;
    direction: ltr;
    border-radius: 5px;
}

.swiper-slide {
    /* padding:50px; */
    text-align: center;
    font-size: 18px;
  background: #fff;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.autoplay-progress {
  position: absolute;
  right: 16px;
  bottom: 16px;
  z-index: 10;
  width: 48px;
  height: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
  margin-right: 20px;
  color: var(--swiper-theme-color);
}

.autoplay-progress svg {
    --progress: 0;
    position: absolute;
    left: 0;
    top: 0px;
    z-index: 10;
  width: 100%;
  height: 100%;
  stroke-width: 4px;
  stroke: var(--swiper-theme-color);
  fill: none;
  stroke-dashoffset: calc(125.6 * (1 - var(--progress)));
  stroke-dasharray: 125.6;
  transform: rotate(-90deg);
}
.swiper-pagination{
    text-align: left;
    transition: 1s all ease;
    margin-left: 20px;
}
.swiper-pagination-bullet{
    padding: 0 8px;
    border-radius: 5px;
    transition: .1s all ease;
    background-color: #fff;
    opacity: 1;
}
.swiper-pagination-bullet:hover{
    background-color: #007aff;
}
.swiper-pagination-bullet-active{
    transition: 1s all ease;
    padding: 0 20px;
    box-shadow: var(--swiper-theme-color) 0px 0px 5px 1px;
    background-color: var(--swiper-theme-color);
}
.SI{ /* Slide Item */
    background-position: center;
    background-size: cover;
}
.timer{
    color:#FFF;
}
.LI{
    width: 100%;
    height: 100%;
    background-image: linear-gradient(rgba(0, 0, 0, 0) , rgba(0, 0, 0, 0.613));
    color:#FFF;
    display: flex;
    justify-content: center;
    align-items: end;
}
</style>