<template>
  <div id="app">
    <ag-charts-vue :options="options"></ag-charts-vue>
  </div>
</template>

<script>
import { AgChartsVue } from "ag-charts-vue";

export default {
  components: {
    AgChartsVue,
  },
  data: function () {
    return {
      options: null,
    };
  },
  created() {
    this.options = {
      autoSize: true,
      title: { text: "Fuel Spending (2019)" },
      data: [
        {
          quarter: "Q1",
          petrol: 200,
          diesel: 100,
        },
        {
          quarter: "Q2",
          petrol: 300,
          diesel: 130,
        },
        {
          quarter: "Q3",
          petrol: 350,
          diesel: 160,
        },
        {
          quarter: "Q4",
          petrol: 400,
          diesel: 200,
        },
      ],
      series: [
        {
          xKey: "quarter",
          yKey: "petrol",
        },
        {
          xKey: "quarter",
          yKey: "diesel",
        },
      ],
    };
  },
  mounted() {},
  methods: {},
};
</script>

<style>
html,
body,
#app {
  height: 100%;
  width: 100%;
  margin: 0;
  box-sizing: border-box;
  -webkit-overflow-scrolling: touch;
}

html {
  position: absolute;
  top: 0;
  left: 0;
  padding: 0;
  overflow: auto;
}

body {
  padding: 1rem;
  overflow: auto;
}
</style>
