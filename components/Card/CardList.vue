<template>
  <Card className="col-12 col-md-5">
    <table class="col-12 table">
      <thead>
        <th>Produto</th>
        <th>Vendas</th>
        <th>Porcentagem</th>
      </thead>
      <tbody>
        <tr v-for="product in products" :key="product.name">
          <td class="col-6">{{product.name}}</td>
          <td class="col-3">{{product.sales}}</td>
          <td class="col-3">{{product.percentage}}%</td>
        </tr>
      </tbody>
    </table>
  </Card>
</template>

<script>
import Card from '../Card/index.vue'
export default {
    name: 'CardList',
    components: {
        Card,
    },
    data() {
        return {
            products: [
                {
                    name: 'Produto 1',
                    sales: 10,
                    percentage: 10
                },
                {
                    name: 'Produto 2',
                    sales: 10,
                    percentage: 10
                },
                {
                    name: 'Produto 3',
                    sales: 10,
                    percentage: 10
                },
                {
                    name: 'Produto 4',
                    sales: 10,
                    percentage: 10
                },
                {
                    name: 'Produto 5',
                    sales: 10,
                    percentage: 10
                }
            ]
        }
    }
}
</script>

<style scoped>
table tr > td{
    background: transparent;
}
</style>
