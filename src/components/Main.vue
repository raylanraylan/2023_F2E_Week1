<script setup>
import AOS from 'aos';
import 'aos/dist/aos.css';

import Cover from './main/Cover.vue';
import News from './main/News.vue';
import Policy from './main/Policy.vue';
import Donation from './main/Donation.vue';
import Public_feedback from './main/Public_feedback.vue'

AOS.init();
</script>
<template>
  <main>
    <Cover data-aos="fade-up"></Cover>
    <News data-aos="fade-up"></News>
    <Policy data-aos="fade-up"></Policy>
    <Donation data-aos="fade-up"></Donation>
    <Public_feedback data-aos="fade-up"></Public_feedback>
  </main>
</template>
<style lang="scss" scoped>

main{
  padding: 60px 0 0;

  @include breakpoint($PC){
    padding: 120px 0 0;
  }
}

</style>