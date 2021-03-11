<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>
<script>

var centerLeft1Data = require("@/adata/data_json/centerLeft1.json")

import Chart from './chart.vue';
export default {
  data () {
    return {
      cdata: {
        xData: [180101, 180701, 190101, 190701, 200101, 200701],
        AS_Num_Data: centerLeft1Data[0][this.country][0],
        Nation_Num_Data: centerLeft1Data[0][this.country][1],
      }
    }
  },
  props: {
    country: String,
    default:{}
  },
  components: {
    Chart,
  },
  watch:{
    country() {
      this.cdata = 
      {
        xData: [180101, 180701, 190101, 190701, 200101, 200701],
        AS_Num_Data: centerLeft1Data[0][this.country][0],
        Nation_Num_Data: centerLeft1Data[0][this.country][1],
      }
    }
  },
  mounted () {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
</style>