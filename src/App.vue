<template>
  <div class="wrapper">
    <h1>chart.js</h1>
    <div class="chart">
      <bar-chart></bar-chart>
    </div>
    <div class="chart">
      <LineChart></LineChart>
    </div>
    <div class="chart">
      <PieChart></PieChart>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import BarChart from "./components/BarChart.vue"
import PieChart from "./components/PieChart.vue"
import LineChart from "./components/LineChart.vue"

export default defineComponent({
  components: {
    BarChart,
    PieChart,
    LineChart
  },
});
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.wrapper {
  padding: 50px;
}
.chart {
  padding: 30px 0;
}
</style>
