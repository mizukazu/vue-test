<template>
  <div id="app">
    <m-header title="Vue テストサイト" :dark="true"></m-header>
    <nav class="nav">
      <ul>
        <li><router-link to="/">ホーム</router-link></li>
        <li><router-link to="/component">カスタムコンポーネント</router-link></li>
      </ul>
    </nav>
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import MHeader from '@/components/MHeader.vue'
export default {
  name: 'app',
  components: {
    MHeader
  }
}
</script>

<style lang="scss">
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.nav {
  background: #6b778d;
  // padding: 30px;
  ul {
    display: flex;
    justify-content: center;
    list-style-type: none;
    margin: 0 0 16px;
    padding: 8px 0;
    li {
      padding: 0 4px;
      a {
        font-weight: bold;
        color: #2c3e50;
        &.router-link-exact-active {
          color: #42b983;
        }
      }
    }
  }
}

.container {
  width: 100%;
  max-width: 960px;
  margin: 0 auto;
  padding: 0 15px;
}
</style>
