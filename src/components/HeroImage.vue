<template>
  <div class="heroImage" />
</template>
<script>
export default {
  name: 'HeroImage',
};
</script>
<style lang="scss" scoped>
.heroImage {
  width: 100%;
  height: 100vh;
  position: fixed;
  z-index: -1;
  top: 0;
  background-image: url('../assets/heroimage.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 80% 0%;

  &::after {
    content: '';
    background: rgba(0, 0, 0, .2);
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
    width: 100%;
    height: 100vh;
  }
}
</style>
