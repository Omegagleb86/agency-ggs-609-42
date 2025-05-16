<script setup>
// core version + navigation, pagination modules:
import Swiper from 'swiper';
import { Navigation, Pagination } from 'swiper/modules';

// import Swiper and modules styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

import { onMounted, ref } from 'vue';

const portfolioCards = ref([
  {
    title: 'Design Byte App',
    ip: 'portfolio__group__item-1',
  },
  {
    title: 'Cloud App',
    ip: 'portfolio__group__item-2',
  },
  {
    title: 'Design Furniture App',
    ip: 'portfolio__group__item-3',
  },
])



onMounted(() => {
  // init Swiper:
  const swiper = new Swiper('.portfolio-swiper', {
    // configure Swiper to use modules
    modules: [Navigation, Pagination],
    // // Optional parameters
    // direction: 'vertical',
    // loop: true,

    // If we need pagination
    pagination: {
      el: '.swiper-pagination',
      clickable: true,
    },

    // Navigation arrows
    navigation: {
      nextEl: '.swiper-button-next',
      prevEl: '.swiper-button-prev',
    },

    // And if we need scrollbar
    // scrollbar: {
    //   el: '.swiper-scrollbar',
    // },
  });
})

</script>

<template>
  <section class="portfolio">
    <div class="container">
      <img src="@/assets/img/dots_right.svg" alt="">
      <img src="@/assets/img/dots_left.svg" alt="">
      <div class="portfolio__group">
        <a href="#">Our Portfolio</a>
        <h2>What do we do</h2>
        <p>all projects that we have already done , proven can help to use more comfortable, then can used
          by
          client from our business</p>


        <!-- Slider main container -->
        <div class="swiper portfolio-swiper">
          <!-- Additional required wrapper -->
          <div class="swiper-wrapper">
            <!-- Slides -->
            <div class="swiper-slide" v-for="item in portfolioCards">
              <div v-bind:id="item.ip" class="portfolio__group__item">
                <!-- <p>Design Byte App</p> -->
                <p>{{item.title}}</p>
              </div>
            </div>
            <!-- <div class="swiper-slide">
              <div id="portfolio__group__item-2" class="portfolio__group__item">
                <p>Cloud App</p>
              </div>
            </div>
            <div class="swiper-slide">
              <div id="portfolio__group__item-3" class="portfolio__group__item">
                <p>Design Furniture App</p>
              </div>
            </div> -->
          </div>
          <!-- If we need pagination -->
          <div class="swiper-pagination"></div>

          <!-- If we need navigation buttons -->
          <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div>

          <!-- If we need scrollbar -->

        </div>
        <!--
                <div class="portfolio__group__cards">
                  <div class="portfolio__group__item">
                    <p>Design Byte App</p>
                  </div>
                  <div class="portfolio__group__item">
                    <p>Cloud App</p>
                  </div>
                  <div class="portfolio__group__item">
                    <p>Design Furniture App</p>
                  </div>
                </div>
                <div class="portfolio__group__cards portfolio__group__cards-mobile">
                  <div class="portfolio__group__item">
                    <p>Design Byte App</p>
                  </div>
                  <div class="portfolio__group__item">
                    <p>Cloud App</p>
                  </div>
                  <div class="portfolio__group__item">
                    <p>Design Furniture App</p>
                  </div>
                </div> -->
        <button class="button-primary">See All Portfolio</button>
      </div>
    </div>
  </section>
</template>

<style scoped></style>
