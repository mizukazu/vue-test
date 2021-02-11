<template>
  <article class="card">
    <figure>
      <img :src="imgUrl" alt="">
    </figure>
    <div class="card-body">
      <h2 class="card-title">カードタイトル</h2>
      <p class="card-text">
        ダミーテキストダミーテキストダミーテキストダミーテキスト
        ダミーテキストダミーテキストダミーテキストダミーテキスト
        ダミーテキストダミーテキストダミーテキストダミーテキスト
      </p>
    </div>
  </article>
</template>

<script>
export default {
  name: 'm-card',
  props: {
  },
  data() {
    return {
      imgUrl: require('../assets/img/computer.jpg')
    }
  },
  created() {
  }
}
</script>

<style scoped lang="scss">
.card {
  width: 100%;
  max-width: 320px;
  border: 1px solid #ccc;
  box-shadow: 0 3px 6px rgba(0,0,0,0.2);
  figure {
    margin: 0;
    img {
      width: 100%;
    }
  }
  .card-body {
    padding: 4px 16px;
    .card-title {
      font-size: 1.3rem;
      margin: 0;
      // padding: 0 8px;
      text-align: left;
    }
    .card-text {
      font-size: 1rem;
      margin: 8px 0;
      // padding: 4px 16px;
    }
  }
}
</style>