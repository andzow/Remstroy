<template>
  <div>
    <MainRsMain/>
    <MainRsAbout/>
    <MainRsServices/>
    <MainRsBanner/>
    <MainRsBlog/>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "Ремстрой – Ремонт под ключ вашего пространства | Ремстрой",
  ogTitle: "Ремстрой - Ремонт под ключ с гарантией качества",
  description:
    "Добро пожаловать на официальный сайт Ремстрой! Мы специализируемся на ремонте под ключ, превращая старые объекты в новые шедевры. Качественно, быстро и с гарантией обновим любое помещение.",
  ogDescription:
    "Ремстрой – ваш надежный партнер в ремонте под ключ. Мы качественно и быстро обновим любое пространство, гарантируя отличный результат и индивидуальный подход к каждому проекту.",
  ogImage: "/Main/banner.webp",
});
</script>