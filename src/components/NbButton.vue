<template>
  <button>
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
  height: 50px;
  width: 190px;
  border-radius: 2px;
  border: 3px solid #2d2d2d;
  font-size: 1.2rem;
  background-color: #f1c34a;
  cursor: pointer;
  font-weight: 700;
}
</style>
