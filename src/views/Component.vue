<template>
  <div class="component">
    <h1>カスタムコンポーネントをテストするページ</h1>
    <div class="component_groups">
      <h2>カード</h2>
      <button @click="show=!show">切り替え</button>
      <transition appear>
         <m-card v-show="show" />
      </transition>
    </div>
  </div>
</template>

<script>
import MCard from '@/components/MCard.vue'
export default {
  name: 'component',
  components: {
    MCard
  },
  data() {
    return {
      show: true
    }
  }
}
</script>

<style scoped lang="scss">
.v-enter-active,
.v-leave-active {
  transition: opacity 1s;
}
.v-enter,
.v-leave {
  opacity: 0;
}
.v-move {
  transition: transform 1s;
}

.component {
  display: flex;
  flex-direction: column;
  h1 {
    font-size: 1.5rem;
  }
}
</style>