<template>
  <div class="goods">
    <h3>商品</h3>
    <nuxt-link to="/goods/1?a=1&b=2">商品01</nuxt-link>
    <nuxt-link
      :to="{ name: 'goods-id', params: { id: 2 }, query: { a: 1, b: 2 } }"
      >商品02</nuxt-link
    >
    <nuxt-link
      :to="{ name: 'goods-id', params: { id: 3 }, query: { a: 3, b: 4 } }"
      >商品03</nuxt-link
    >
    <nuxt-link to="goods/comment">评论</nuxt-link>
    <nuxt />
  </div>
</template>
<script>
export default {
  head() {
    return {
      meta: [{ name: "keywords", content: this.title }]
    };
  },
  data() {
    return {
      title: "商品主页"
    };
  }
};
</script>
