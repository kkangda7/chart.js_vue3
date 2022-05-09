<template>
  <div class="chart">
    <LineChart :chartData="lineData" />
  </div>
</template>

<script>
import { Chart, registerables } from "chart.js";
import { defineComponent } from "vue";
import { LineChart } from "vue-chart-3";

Chart.register(...registerables);

export default defineComponent({
  components: {
    LineChart
  },
  setup(){
    const lineData = {
      labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul"],
      datasets: [
        {
          label: "My First Dataset",
          data: [65, 59, 80, 81, 56, 55, 40],
          fill: true,
          borderColor: "rgb(75, 192, 192)",
          tension: 0.1,
        },
      ],
    };
    return {
      lineData
    }
  }
})
</script>

<style>

</style>