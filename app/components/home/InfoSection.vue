<template>
  <section class="py-10 px-4 max-w-screen-xl mx-auto">
    <!-- Icons row -->
    <div
      class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-5 gap-6 text-center mb-10"
    >
      <div v-for="(icon, index) in icons" :key="index">
        <img :src="icon.image" alt="" class="mx-auto h-16" />
        <p class="mt-2 text-sm font-semibold">{{ icon.label }}</p>
      </div>
    </div>

    <!-- Banners -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      <div v-for="(banner, index) in banners" :key="index">
        <img :src="banner.image" alt="" class="rounded-xl shadow-md" />
      </div>
    </div>
  </section>
</template>

<script setup>
const icons = [
  { image: "images/giao-hang-tan-nha.png", label: "GIAO HÀNG TẬN NHÀ" },
  { image: "images/boc-qua-gia-re.png", label: "BỌC QUÀ GIÁ RẺ" },
  { image: "images/tang-thiep-mien-phi.png", label: "TẶNG THIỆP MIỄN PHÍ" },
  { image: "images/giat-gau-bog.png", label: "GIẶT GẤU BÔNG" },
  { image: "images/nen-nho-gau.png", label: "NÉN NHỎ GẤU" },
];

const banners = [
  { image: "images/gau_1.png" },
  { image: "images/gau_2.png" },
  { image: "images/gau_3.png" },
  { image: "images/gau_4.png" },
  { image: "images/gau_5.png" },
  { image: "images/gau_6.png" },
];
</script>
