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
    data(){
      return{
        dataS:[
          {src:'slide_4',title:'چرخه زندگی در ری اکت - مباحث مقدماتی',time:'3 هفته پیش',views:564,category:'ری اکت'},
          {src:'photo_1_2023-06-14_12-33-11',title:'آموزش ساخت api به  صورت همزمان و اتصال دو طرفه',time:'6 روز پیش',views:211,category:'نود جی اس'},
          {src:'photo_2023-06-14_12-49-30',title:'ویو جی اس یا انگولار - کدام یک سریع تر و کدام یک کار آمد تر',time:'4 ماه پیش',views:3752,category:'فریمورک'},
          {src:'d619a64645bf2cbf8f32f9063cf29ac5',title:'نقشه راه ورود به دنیای طراحی وب',time:'1 سال پیش',views:9800,category:'وب'},
        ]
      }
    },
    components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      return {
        modules: [Autoplay, Pagination, Navigation],
      };
    },
  };

</script>
<template>
    <div class="CS">
      <swiper
      loop="true"
      speed="2000"
      :spaceBetween="30"
      :centeredSlides="true"
      :autoplay="{
        delay: 3000,
        disableOnInteraction: false,
      }"
      :pagination="{
        clickable: true,
      }"
      :modules="modules"
      @autoplayTimeLeft="onAutoplayTimeLeft"
      class="mySwiper"
    >
      <swiper-slide v-for="item in dataS" class="SI" :style="`background-image:url(${item.src}.jpg);`">
        <div class="LI">
          <router-link to="/" class="TS">{{ item.title }}</router-link>
          <div class="DS">
            <div class="DSI">
              <div class="fontIcon">&#xe902</div>
              <div><span>دسته : </span>{{ item.category }}</div>
            </div>
            <div class="DSI">
              <div class="fontIcon">&#xe904</div>
              <div>{{ item.views }} نفر</div>
            </div>
            <div class="DSI">
              <div class="fontIcon">&#xe903</div>
              <div>{{ item.time }}</div>
            </div>
          </div>
        </div>
      </swiper-slide>
      
      <template #container-end>
        <div class="autoplay-progress">
          <svg viewBox="0 0 48 48" ref="progressCircle">
            <circle cx="24" cy="24" r="20"></circle>
          </svg>
        </div>
      </template>
    </swiper>
  </div>
</template>
<style>
.CS{ /* Container Swiper */
  box-shadow: rgba(0, 0, 0, 0.2) 0px 20px 30px;
  margin:30px 20px ;

}
.swiper {
  height: 600px;
  width:100%;
  direction: ltr;
  border-radius: 15px;
}

.swiper-slide {
  /* padding:50px; */
  text-align: center;
  font-size: 18px;
  background: #fff;
  border-radius: 15px;
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
  margin-left: 55px;
  margin-bottom: 20px;
}
.swiper-pagination-bullet{
  transition: 1s all ease;
  padding: 5px 8px;
  border-radius: 15px;
  transition: .1s all ease;
  background-color: #fff;
  opacity: 1;
}
.swiper-pagination-bullet:hover{
  background-color: #007aff;
}
.swiper-pagination-bullet-active{
  transition: 1s all ease;
  padding: 5px 20px;
  box-shadow: var(--swiper-theme-color) 0px 0px 5px 1px;
  background-color: var(--CB);
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
  background-image: linear-gradient(rgba(0, 0, 0, 0) , rgba(0, 0, 0, 0.774));
  color:#FFF;
  display: flex;
  flex-direction: column;
  justify-content: end;
  gap:40px;
  padding:20px 60px;
  align-items: end;
}
.TS{ /* Title Slider */
  font-family: vazirBold;
  font-size: 28px;
  transition: .1s all ease;
}
.TS:hover{
  color:var(--CB);
}
.DS{ /* Description Slide */
  display: flex;
  gap:30px;
}
.DSI{ /* Description Slide Item */
  display: flex;
  align-items: center;
  gap:8px;
  direction: rtl;
  font-size: 15px;
}
.DSI .fontIcon {
  font-size: 22px;
}
</style>