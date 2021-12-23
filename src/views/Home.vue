<template>
  <div>
    <Hero />
    <FirstSection />
    <SecondSection />
    <Third />
    <Banner />
    <Fourth />
    <Astro />
  </div>
</template>

<script>
import Hero from "@/components/Hero.vue";
import FirstSection from "@/components/FirstSection.vue";
import SecondSection from "@/components/SecondSection.vue";
import Third from "@/components/Third.vue";
import Banner from "@/components/Banner.vue";
import Fourth from "@/components/Fourth.vue";
import Astro from "@/components/Astro.vue";

export default {
  name: "Home",
  components: {
    Hero,
    FirstSection,
    SecondSection,
    Third,
    Banner,
    Fourth,
    Astro,
  },
};
</script>
