<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from './chart.vue';
import Vue from "vue";
export default {
  data () {
    return {
      cdata: [],
    }
  },
  components: {
    Chart,
  },
  methods: {},
  mounted() {
    var container = document.getElementById("centreLeft2Chart");
    var chart = this.$echarts.init(container);
    // console.log(chart)
    chart.on("timelinechanged", function (params) {
      var currentIndex = params.currentIndex + 2015;
      // sessionStorage.setItem("currentIndex", currentIndex);
      Vue.prototype.resetSetItem("currentIndex", currentIndex);
    });
    chart.on("click",  (params) => {
      var currentName = params.data.name;
      this.$emit('transmitCountry1',currentName)
      // this.$emit('transmitYear', currentIndex)
      // console.log(currentName + "1")
    });

  },
}
</script>

<style lang="scss" scoped>
</style>