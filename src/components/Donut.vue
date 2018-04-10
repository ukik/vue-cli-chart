<template>
  <GridLayout rows="*" height="1000px">
    <RadPieChart allowAnimation="true" row="0">
      <DonutSeries v-tkPieSeries selectionMode="DataPoint" expandRadius="0.4" outerRadiusFactor="0.7" innerRadiusFactor="0.4" :items="pieSource" valueProperty="Amount" legendLabel="Brand" />
      <RadLegendView v-tkPieLegend position="Right" title="Brands" offsetOrigin="TopRight" width="110" enableSelection="true" />
    </RadPieChart>
  </GridLayout>
</template>

<script>
  
  require("../nativescript-vue/chart-directives");
  const Vue = require("nativescript-vue");

  export default {
    data() {
      return {
        pieSource: [{
            Brand: "Audi",
            Amount: 10
          },
          {
            Brand: "Mercedes",
            Amount: 76
          },
          {
            Brand: "Fiat",
            Amount: 60
          },
          {
            Brand: "BMW",
            Amount: 24
          },
          {
            Brand: "Crysler",
            Amount: 40
          }
        ],
      }
    },
  } //.$start();
</script>

