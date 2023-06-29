<template>
  <Card className="col-12 mt-3">
    <h5>Total de vendas - Últimos 12 meses</h5>
    <LineChart
      :chart-options="chartOptions"
      :chart-data="chartData"
      :width="700"
      :height="400"
    />
  </Card>
</template>

<script>
import Card from '../Card/index.vue'

export default {
  name: 'CardSales',
  components: {
    Card,
  },
  props: {
    chartId: {
      type: String,
      default: 'line-chart',
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
          'Abr/2022',
          'Fev/2022',
          'Abr/2022',
          'Mai/2022',
          'Jun/2022',
          'Jul/2022',
          'Ago/2022',
          'Set/2022',
          'Out/2022',
          'Nov/2022',
          'Dez/2022',
          'Jan/2023',
          'Fev/2023',
          'Mar/2023',
          'Abr/2023',
          'Mai/2023',
          'Jun/2023',
          'Jul/2023',
        ],
        datasets: [
          {
            label: 'N° vendas',
            backgroundColor: '#4b4bf9',
            borderColor: '#4b4bf9',
            data: [
              750, 740, 680, 810, 600, 660, 580, 0, 0, 0, 0, 0, 0, 600, 700,
              520, 750, 680,
            ],
            tension: 0.4,
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
