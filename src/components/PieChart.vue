<template>
  <div class="chart">
      <PieChart :chartData="pieData" />
  </div>
</template>

<script>
import { Chart, registerables } from "chart.js";
import { defineComponent } from "vue";
import { PieChart } from "vue-chart-3";

Chart.register(...registerables);

export default defineComponent({
  components: {
    PieChart
  },
  setup(){
    const pieData = {
      labels: ["Red", "Blue", "Yellow"],
      datasets: [
        {
          label: "My First Dataset",
          data: [300, 50, 100],
          backgroundColor: [
            "rgb(255, 99, 132)",
            "rgb(54, 162, 235)",
            "rgb(255, 205, 86)",
          ],
          hoverOffset: 4,
        },
      ],
    };
    return { pieData };
  }
})
</script>

<style>

</style>