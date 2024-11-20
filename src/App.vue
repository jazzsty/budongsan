<template>
  <div class="menu">
    <!-- <a href="" v-for="menu in 3" :key="menu">HOME</a> -->
    <a href="" v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>
  <div class="main" :style="attr1">
    <h4>{{ products[0] }}</h4>
    <p>{{ prices[0]}} 만원</p>
    <button v-on:click="count[0]++">허위매물신고</button> <span>신고수: {{ count[0] }}</span>
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ prices[1] }} 만원</p>
    <button v-on:click="count[1]++">허위매물신고</button> <span>신고수: {{ count[1] }}</span>
  </div>
  <div>
    <h4>{{ products[2] }}</h4>
    <p>{{ prices[2] }} 만원</p>
    <button v-on:click="count[2]++">허위매물신고</button> <span>신고수: {{ count[2] }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: [0, 0, 0],
      prices: [80, 70, 100],
      products: ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      attr1: 'color: blue;',
      menus: ['Home', 'products', 'about'],
    }
  },
  methods: {
    increase() {
      this.count += 1;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}
.menu {
  background-color: blue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
