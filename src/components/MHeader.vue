<template>
  <header :class="{ dark: this.dark }">
    <h1>{{ title }}</h1>
    <slot></slot>
  </header>
</template>

<script>
export default {
  name: 'm-header',
  props: {
    title: String,
    dark: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
    }
  },
  created() {
    console.log(this.dark)
  }
}
</script>

<style scoped lang="scss">
header {
  background: #add6ff;
  color: #333;
  padding: 8px 8px;
  h1 {
    margin: 0;
  }
}
header.dark {
  background: #17223b;
  color: #fff;
}
</style>