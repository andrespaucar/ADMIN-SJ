<template>
  <button class="btn " :block="block"
    :class="[`btn-${color}`, size? `btn-${size}`:'']"
    :type="type">
      <slot></slot>
  </button>
</template>

<script>
export default {
    props:{
        color:{default:'default',required:false},
        size:{required:false},
        type:{default:'button',required:false},
        block:{required:false},
    }
}
</script>

<style>

</style>