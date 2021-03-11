<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from './chart.vue';
export default {
  data () {
    return {
      cdata: {
        x_Data: [
                180101,
                180701,
                190101,
                190701,
                200101,
                200701,
                ],
        bar_Data: [261340, 312994, 318997, 345300, 360035, 336446],
        
        line_Data: [59147, 61055, 62891, 65101, 67279, 69291],
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