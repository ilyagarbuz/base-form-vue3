<template>
  <input
    type="radio"
    :checked="value === modelValue"
    :value="value"
    @change="$emit('update:modelValue', $event.target.value)"
    v-bind="$attrs"
  />
  <label v-if="label">{{label}}</label>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: ''
    },
    modelValue: {
      type: [String, Number],
      default: ''
    },
    value: {
      type: [String, Number],
      required: true
    }
  }
}
</script>
