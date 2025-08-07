<template>
  <section class="py-10 px-4 max-w-screen-xl mx-auto">
    <h2 class="text-2xl font-bold text-center text-pink-500 mb-6">
      BST CAPYBARA
    </h2>
    <Swiper
      :slides-per-view="1.5"
      :space-between="20"
      :breakpoints="{
        640: { slidesPerView: 1.5 },
        768: { slidesPerView: 2.5 },
        1024: { slidesPerView: 3.5 },
        1280: { slidesPerView: 4 },
      }"
    >
      <SwiperSlide v-for="(item, index) in products" :key="index">
        <div class="bg-white shadow-lg rounded-xl overflow-hidden">
          <img
            :src="item.image"
            :alt="item.title"
            class="w-full h-[200px] object-cover rounded-t-xl"
          />
          <div class="p-4">
            <h3 class="text-base font-semibold text-gray-800 mb-1">
              {{ item.title }}
            </h3>
            <p class="text-pink-500 font-bold text-lg mb-3">
              {{ item.price }}
              <span class="text-sm">₫</span>
            </p>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="(size, sIndex) in item.sizes"
                :key="sIndex"
                class="text-pink-500 border border-pink-300 text-sm px-3 py-1 rounded-full"
              >
                {{ size }}
              </span>
            </div>
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";

const products = [
  {
    title: "Chuột Capybara Đội Mũ Dâu",
    price: "245,000",
    image: "images/bong_2.png",
    sizes: ["35cm", "45cm", "55cm", "70cm", "90cm"],
  },
  {
    title: "Chuột Capybara Nước Mũi",
    price: "225,000",
    image: "images/bong_1.png",
    sizes: ["30cm", "40cm", "50cm", "65cm"],
  },
  {
    title: "Gấu Bông Capybara Tiên Cá",
    price: "95,000",
    image: "images/bong_3.png",
    sizes: ["23cm", "30cm", "45cm", "75cm"],
  },
  {
    title: "Gấu Bông Capybara Cosplay Cá Mập",
    price: "275,000",
    image: "images/bong_4.png",
    sizes: ["45cm", "60cm", "80cm", "1m"],
  },
  {
    title: "Chuột Capybara Đội Mũ Dâu",
    price: "245,000",
    image: "images/bong_2.png",
    sizes: ["35cm", "45cm", "55cm", "70cm", "90cm"],
  },
  {
    title: "Chuột Capybara Nước Mũi",
    price: "225,000",
    image: "images/bong_1.png",
    sizes: ["30cm", "40cm", "50cm", "65cm"],
  },
  {
    title: "Gấu Bông Capybara Tiên Cá",
    price: "95,000",
    image: "images/bong_3.png",
    sizes: ["23cm", "30cm", "45cm", "75cm"],
  },
  {
    title: "Gấu Bông Capybara Cosplay Cá Mập",
    price: "275,000",
    image: "images/bong_4.png",
    sizes: ["45cm", "60cm", "80cm", "1m"],
  },
];
</script>
