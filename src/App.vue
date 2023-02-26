<template>
  <hero />
  <nb-benefits />
  <nb-how-works />
</template>

<script>
import Hero from "./components/Hero.vue";
import NbBenefits from "./components/NbBenefits.vue";
import NbHowWorks from "./components/NbHowWorks.vue";
export default {
  name: "App",
  components: { Hero, NbBenefits, NbHowWorks },
};
</script>

<style>
* {
  font-family: "Sarabun", sans-serif;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  color: #2d2d2d;
}
.contrast {
  color: #9a4725;
  font-weight: 600;
}
</style>
