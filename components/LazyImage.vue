<template>
  <img v-lazy-load :src="src.placeholder" :data-srcset="src.srcSet" />
</template>

<script>
export default {
  props: {
    src: {
      type: Object,
      required: true
    }
  }
}
</script>
