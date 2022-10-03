<template>
  <component
    v-for="option in options"
    :key="option.value"
    :is="vertical ? 'div' : 'span'"
    :class="{'horizontal': !vertical}"
  >
      <BaseRadio
        :name="name"
        :value="option.value"
        :label="option.label"
        :modelValue="modelValue"
        @change="$emit('update:modelValue', $event.target.value)"
      />
  </component>
</template>

<script>
export default {
  props: {
    options: {
      type: Array,
      require: true
    },
    name: {
      type: String,
      require: true
    },
    modelValue: {
      tpye: [String, Number],
      require: true
    },
    vertical: {
      type: Boolean,
      require: true
    }
  }
}
</script>

<style scoped>
  .horizontal {
    margin-right: 20px;
  }
</style>
