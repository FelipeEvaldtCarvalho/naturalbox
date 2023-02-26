<template>
  <button :class="{ full: fullWidth }">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "NbButton",
  props: {
    fullWidth: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
button {
  border-radius: 0.3vw;
  border: 0.2vw solid #2d2d2d;
  font-size: 1.4vw;
  background-color: #f1c34a;
  cursor: pointer;
  font-weight: 700;
  padding: 1.1vw 4.4vw;
}
.full {
  width: 100%;
}
@media screen and (max-width: 735px) {
  button {
    border-radius: 0.6vw;
    border: 0.4vw solid #2d2d2d;
    font-size: 4.4vw;
    padding: 3.3vw 9.9vw;
  }
}
</style>
