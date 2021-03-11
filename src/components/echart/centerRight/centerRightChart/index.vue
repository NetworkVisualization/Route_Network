<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>
<script>

var centerRightData = require("@/adata/data_json/centerRight.json")

import Chart from './chart.vue';
export default {
  data () {
    return {
      cdata: {
        indicatorData: [{
                    name: '可信性',
                    max: 1000,
                }, {
                    name: '容错性',
                    max: 1000
                }, {
                    name: '可靠性',
                    max: 1000
                }, {
                    name: '安全性',
                    max: 1000
                }, {
                    name: '可生存性',
                    max: 1000
                }],
        
        data_test:centerRightData[0][this.country],

      }
    }
  },
  props: {
    country: String,
    default:{}
  },
  watch: {
    country() {
      this.cdata = {
        indicatorData: [{
                    name: '可信性',
                    max: 1000,
                }, {
                    name: '容错性',
                    max: 1000
                }, {
                    name: '可靠性',
                    max: 1000
                }, {
                    name: '安全性',
                    max: 1000
                }, {
                    name: '可生存性',
                    max: 1000
                }],
        
        data_test:centerRightData[0][this.country],

      }
    }
  },
  components: {
    Chart,
  },
  mounted () {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
</style>