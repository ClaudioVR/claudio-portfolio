<template>
  <section>
    <div class="chart">
      <BubbleChart :data="datacollection" :options="options" :height="200" />
    </div>
  </section>
</template>

<script>
import { Bubble } from 'vue-chartjs'
export default {
  extends: Bubble,
  data() {
    return {
      datacollection: {
        labels: ['Data'],
        datasets: [
          {
            label: 'Charts.js is an amazing tool',
            backgroundColor: 'rgba(33,150,243, 0.5)',
            pointBackgroundColor: 'white',
            borderWidth: 1,
            pointBorderColor: '#249EBF',
            data: [
              {
                x: 100,
                y: 0,
                r: 10
              },
              {
                x: 60,
                y: 30,
                r: 20
              },
              {
                x: 40,
                y: 60,
                r: 25
              },
              {
                x: 80,
                y: 80,
                r: 50
              },
              {
                x: 20,
                y: 30,
                r: 25
              },
              {
                x: 0,
                y: 100,
                r: 5
              }
            ]
          }
        ]
      },
      options: {
        scales: {
          yAxes: [{
            ticks: {
              beginAtZero: true
            },
            gridLines: {
              display: true
            }
          }],
          xAxes: [{
            gridLines: {
              display: false
            }
          }]
        },
        legend: {
          display: true
        },
        responsive: true,
        maintainAspectRatio: true
      }
    }
  },
}
</script>

<style scoped>
/* .title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 400;
  font-size: 100px;
  color: #2e495e;
  letter-spacing: 1px;
  font-size: 6em;
}
.green {
  color: #00c48d;
}

.subtitle {
  font-weight: 300;
  font-size: 1em;
  color: #2e495e;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
} */
</style>
