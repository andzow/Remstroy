<template>
  <div>
    <UIRsHeader />
    <main>
      <NuxtPage />
    </main>
    <UIRsFooter/>
  </div>
</template>

<script>
import AOS from "aos";
import 'aos/dist/aos.css';

export default {
  mounted() {
    if (process.client) {
      AOS.init();
    }
  },
}
</script>
