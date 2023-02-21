<template>
  <input @input="updateValue" :value="modelValue"/>
</template>

<script>
  export default {
  props: {
      modelValue: [Number, String]
  },
  methods: {
    updateValue (event)
    {
      this.$emit('update:modelValue', event.target.value)
    }
  }
  }
</script>

<style lang="scss" scoped>

</style>