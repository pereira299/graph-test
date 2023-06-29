<template>
  <Layout>
    <h3 class="mb-1">
      Histórico
    </h3>
    <hr class="col-12"/>
    <div class="d-flex flex-row justify-content-between flex-wrap">
      <card-product></card-product>
      <card-list></card-list>
    </div>
    <card-sales></card-sales>
  </Layout>
</template>

<script lang="ts">
import Vue from 'vue'
import CardProduct from '../components/Card/CardProduct.vue'
import CardList from '../components/Card/CardList.vue'
import Layout from '../components/template/Layout.vue'
import CardSales from '../components/Card/CardSales.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Layout,
    CardProduct,
    CardSales
  }, 
  head: {
    title: 'Manfing | Histórico',
    meta: [
      { hid: 'description', name: 'description', content: 'Histórico' },
    ],
    link: [{ rel: 'icon', type: 'image/png', href: '/logo.png' }],
  }
})
</script>

<style scoped>
  hr {
    border-bottom: 1px solid #9c9c9c;
  }
  body {
    background: #fff;
  }
</style>
