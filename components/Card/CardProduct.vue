<template>
  <Card className="col-12 col-md-6 mb-3 mb-md-0">
    <h5>Venda por produtos - Todo período</h5>
    <DoughnutChart
      :chart-options="chartOptions"
      :chart-data="chartData"
      :width="500"
      :height="250"
    />
  </Card>
</template>

<script>
import Card from '../Card/index.vue'

export default {
  name: 'CardProduct',
  components: {
    Card,
  },
  props: {
    chartId: {
      type: String,
      default: 'doughnut-chart',
    },
    datasetIdKey: {
      type: String,
      default: 'label',
    },
    width: {
      type: Number,
      default: 400,
    },
    height: {
      type: Number,
      default: 400,
    },
    cssClasses: {
      default: '',
      type: String,
    },
    styles: {
      type: Object,
      default: () => {},
    },
    plugins: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      chartData: {
        labels: [
          'CANTONEIRAS ESP. - PF20-11',
          'CANTONEIRAS ESP. - PF20-12',
          'CANTONEIRAS ESP. - PF20-11-PP',
          'ITENS PLAST. - PF30-11',
          'CANTONEIRAS ESP. - PF20-12-PP',
          'CANTONEIRAS - CTA20-01',
          'PRODUTO FINAl - PMT20-05-10',
          'ITENS PLAST. - PF40-01',
          'PERFIS ESP. - PFT30-01',
          'CANTONEIRAS ESP. - PF20-14',
        ],
        datasets: [
          {
            backgroundColor: [
              "#50478a",
              "#514ba3",
              "#5454bd",
              "#4f4fd6",
              "#6666fa",
              "#ce2626",
              "#e53535",
              "#ff5757",
              "#f66126",
              "#ff8826",

            ],
            data: [30, 10, 5, 5, 10, 5, 5, 5, 15, 5],
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
      },
    }
  },
}
</script>
