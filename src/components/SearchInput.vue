<template>
  <input
    id="search"
    name="search"
    :class="{ dark }"
    :value="value"
    @input="handleChange"
  />
</template>
<script>
  export default {
    name: 'SearchInput',
    props: {
      value: {
        type: String,
        required: true,
      },
      dark: {
        type: Boolean,
        default: false,
      },
    },
    methods: {
      handleChange(e) {
        this.$emit('input', e.target.value);
      },
    },
  };
</script>
<style lang="scss" scoped>
input {
  margin-top: 50px;
  height: 30px;
  color: white;
  text-align: center;
  font-size: 18px;
  border: 0;
  border-bottom: 1px solid white;
  background: none;
  transition: box-shadow .3s ease-out;

  @media (min-width: 1024px) {
    font-weight: 400;
  }

  &:focus {
    outline: none;
    box-shadow: 0 10px 20px -8px rgba(255, 255, 255, .5);
  }
}
.dark {
  color: #1e3d4a;
  border-bottom-color: #1e3d4a;

  &:focus {
    box-shadow: 0 10px 20px -8px rgba(#1e3d4a, .2);
  }
}

label {
  font-family: "Montserrat", sans-serif;
}
</style>
