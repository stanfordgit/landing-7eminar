<template>
  <div class="v-input">
    <div v-if="label" class="v-input__label">{{ label }}</div>
    <input 
      :type="type"
      :placeholder="placeholder" 
      :class="{ 'is-invalid': !isValid }"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"/>
    <p v-if="!isValid && errorMessage != ''" class="error-message">{{ errorMessage }}</p>
  </div>
</template>

<script setup>

const emits = defineEmits(['update:modelValue'])
const props = defineProps({
  type: {
    type: String,
    required: false,
    default: ''
  },
  modelValue:{
    type: String,
    default: ''
  },
  placeholder: {
    type: String,
    required: false,
    default: ''
  },
  label:{
    type: String,
    required: false,
    default: ''
  },
  isValid:{
    type: Boolean,
    required: false,
    default: false,
  },
  errorMessage:{
    type: String,
    required: false,
    default: ''
  }
})
</script>

<style lang="scss" scoped>
.v-input{
  display: flex;
  flex-direction: column;
  &__label{
  font-family: "Raleway", sans-serif;
  font-size: 16px;
  font-weight: 400;
  margin-bottom: 7px;
  }
  input{
    padding: 17px 24px;
    border-radius: 32px;
    border: 1px solid $color-black-content;
    
    outline: none;
    width: 100%;
    background: $color-background;
    &::placeholder{
      color: #858585;
      font-family: 'Raleway', sans-serif;
      font-size: 16px;
      font-weight: 400;

      opacity: 0.7;
    }
  }
  &.tariff{
    input{
      
    }
  }
}


.error-message {
  color: red;
  font-size: 14px;
  margin-top: 5px;
}
</style>