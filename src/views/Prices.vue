<template>
  <div>
    <PriceTop />
    <TableSection />
    <Astro />
  </div>
</template>

<script>
import Astro from "@/components/Astro.vue";
import TableSection from "../components/TableSection.vue";
import PriceTop from "../components/PriceTop.vue";

export default {
  name: "Prices",
  components: { Astro, TableSection, PriceTop },
};
</script>

<style>
</style>