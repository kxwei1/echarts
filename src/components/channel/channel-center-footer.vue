<template>
  <div class="footer">
    <div id="channel-center-footer"></div>
  </div>
</template>

<script>
import echarts from "echarts";

export default {
  components: {},
  props: {},
  data() {
    return {};
  },
  mounted() {
    var myChart = echarts.init(
      document.getElementById("channel-center-footer")
    );
    let data = {
      rain: [8, 18, 8, 12, 0, 19, 21, 19, 24.8, 23, 29.7],
      tmp: [12, 13, 9.7, 8, -6, 15, 25, 15, 23, 14, 23],
      winds: [3, 2.8, 5, 6.8, 6.4, 8, 7, 8.4, 7, 8, 10],
      pre: [600, 400, 550, 580, 400, 500, 700, 500, 600, 700, 650],
    };

    let colors = ["#3597cc", "#4aabbe", "#a2345c", "#9dc72b"];
    let splitNumber = 5; // 分割段数

    var option = {
      color: colors,
      // backgroundColor: "#fff",
      grid: {
        top: "15%",
        bottom: "10%",
        left: "15%",
        right: "15%",
      },
      legend: {
        top: "9%",
      },
      tooltip: {
        trigger: "axis",
        axisPointer: { type: "shadow" },
      },
      xAxis: {
        type: "category",
        axisTick: { show: false },
        axisLabel: {
          textStyle: { color: "#333333", fontSize: 14 },
        },
        axisLine: {
          show: false,
          lineStyle: { color: "#707070" },
        },
        data: [
          "02",
          "03",
          "04",
          "05",
          "06",
          "07",
          "08",
          "09",
          "10",
          "11",
          "12",
        ],
      },
      yAxis: [
        {
          name: "单位(个)",
          type: "value",
          position: "left",
          splitNumber: splitNumber,
          splitLine: {
            lineStyle: { type: "dashed", color: "#707070" },
          },
          axisLabel: {
            textStyle: { color: colors[0], fontSize: 14 },
          },
          axisLine: { show: false },
          axisTick: { show: false },
        },
        {
          type: "value",
          position: "left",
          offset: 65,
          splitNumber: splitNumber,
          splitLine: { show: false },
          axisLine: { show: false },
          axisLabel: {
            show: false,

            textStyle: { color: colors[1], fontSize: 14 },
          },
          axisTick: { show: false },
        },
        {
          name: "单位(%)",
          type: "value",
          position: "right",
          splitNumber: splitNumber,
          splitLine: { show: false },
          axisLine: { show: false },
          axisLabel: {
            textStyle: { color: colors[3], fontSize: 14 },
          },
          axisTick: { show: false },
        },
        {
          type: "value",
          position: "right",
          offset: 54,
          splitNumber: splitNumber,
          splitLine: { show: false },
          axisLine: { show: false },
          axisLabel: {
            show: false,

            textStyle: { color: colors[2], fontSize: 14 },
          },
          axisTick: { show: false },
        },
      ],
      series: [
        {
          name: "当前值",
          type: "bar",
          barWidth: "40%",
          data: data.rain,
          itemStyle: {
            normal: {
              color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
                {
                  offset: 0,
                  color: "rgba(89,211,255,1)",
                },
                {
                  offset: 1,
                  color: "rgba(23,171,255,1)",
                },
              ]),
            },
          },
        },
        {
          name: "除夕同比",
          type: "line",
          symbol: "none",
          symbolSize: 15,
          yAxisIndex: 1,
          data: data.tmp,
        },
        {
          name: "日环比",
          type: "line",
          symbol: "none",
          symbolSize: 15,
          yAxisIndex: 3,

          data: data.pre,
        },
        {
          name: "日同比",
          type: "line",
          symbol: "none",
          symbolSize: 15,
          yAxisIndex: 2,
          data: data.winds,
        },
      ],
    };
    myChart.setOption(option);
  },
  methods: {},
  computed: {},
  watch: {},
};
</script>

<style  scoped>
.footer,
.footer #channel-center-footer {
  width: 910px;
  height: 500px;
}
</style>
