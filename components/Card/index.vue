<template>
  <article :class="' p-3 rounded ' + this.className">
    <slot></slot>
  </article>
</template>

<script>
export default {
  name: 'Card',
  props: {
    className: {
      type: String,
      default: '',
    },
  },
}
</script>

<style>
    article {
        background: #fff;
    }
</style>
