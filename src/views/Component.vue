<template>
  <div class="component">
    <h1>カスタムコンポーネントをテストするページ</h1>
    <div>
      <h2>カード</h2>
      <m-card/>
    </div>
  </div>
</template>

<script>
import MCard from '@/components/MCard.vue'
export default {
  name: 'component',
  components: {
    MCard
  }
}
</script>

<style scoped lang="scss">
h1 {
  font-size: 1.5rem;
}
</style>