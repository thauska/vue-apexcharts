<template>
  <div>
    <div class="chart-wrapper">
      <apexchart 
        width="500" type="bar" 
        :options="options" :series="series">
      </apexchart>  
    </div>
    <hr>
    <div class="chart-wrapper">
      <apexchart
        width="800" type="line"
        :options="options" :series="series">
      </apexchart>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      options: {
        chart: {
          id: 'vuechart-bar-example'
        },
        xaxis: {
          categories: [
            'Jan',
            'Fev',
            'Mar',
            'Abr',
            'Mai',
            'Jun',
            'Jul',
            'Ago',
            'Set',
            'Out',
            'Nov',
            'Dez',
          ]
        },
        title: {
          text: 'Preço de estoque por mês',
          align: 'center',
          style: {
            fontSize: '14px'
          }
        },
        colors: ['#00897b']
      },
      series: [{
        name: 'series-1',
        data: [55, 62, 89, 66, 98, 72, 101, 75, 94, 120, 117, 139]
      }]
    }
  }
}
</script>

<style scoped>
div.chart-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>