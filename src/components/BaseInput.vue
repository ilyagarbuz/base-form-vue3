<template>
  <label>{{label}}</label>
  <input
    :value="modelValue"
    :placeholder="label"
    class="field"
    v-bind="$attrs"
    @input="$emit('update:modelValue', $event.target.value)"
  >
</template>

<script>
export default {
  props: {
    label: {
      type: [String],
      defautlt: ''
    },
    modelValue: {
      type: [String, Number],
      defautlt: ''
    }
  }
}
</script>
