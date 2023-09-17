<template>
  <button
    :to="to"
    :type="type"
    class="v-button"
    :class="buttonClass"
    @click="onClick"
  >
    <slot />
  </button>
</template>

<script>
export default {
  name: 'VButton',
  props: {
    to: {
      type: String,
      required: false
    },
    type: {
      type: String,
      required: false
    },
    buttonClass: {
      type: String,
      required: false,
      default: 'default'
    },
    onClick: {
      type: Function,
      required: false
    }
  },
};
</script>

<style lang="scss" scoped>
.v-button {
  all: unset;
  display: flex;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  border-radius: 980px;
  transition: background 0.2s ease;


  font-family: "Raleway", sans-serif;
  font-size: 17px;
  font-weight: 600;
  line-height: 20px;
  letter-spacing: -0.374px;

  color: #fff;
  background: $color-blue-primary;

  cursor: pointer;
  &.default{
    padding: 18px 32px;
  }
  &:hover{
    background: $color-blue;
  }
}
</style>
