<template>
  <div class="top">
    <div class="hader">渠道分布</div>
    <div id="channel-right-top"></div>
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
    var myChart = echarts.init(document.getElementById("channel-right-top"));

    var option = {
      // backgroundColor: "#232d36",
      tooltip: {
        trigger: "axis",
        axisPointer: {
          lineStyle: {
            color: {
              type: "linear",
              x: 0,
              y: 0,
              x2: 0,
              y2: 1,
              colorStops: [
                {
                  offset: 0,
                  color: "rgba(0, 255, 233,0)",
                },
                {
                  offset: 0.5,
                  color: "rgba(255, 255, 255,1)",
                },
                {
                  offset: 1,
                  color: "rgba(0, 255, 233,0)",
                },
              ],
              global: false,
            },
          },
        },
      },
      grid: {
        top: "15%",
        left: "10%",
        right: "5%",
        bottom: "15%",
        // containLabel: true
      },
      xAxis: [
        {
          type: "category",
          axisLine: {
            show: false,
            color: "#A582EA",
          },

          axisLabel: {
            color: "#A582EA",
            width: 100,
          },
          splitLine: {
            show: true,
            lineStyle: {
              color: "#00BFF3",
              opacity: 0.23,
            },
          },
          boundaryGap: false,
          data: [
            "1",
            "2",
            "3",
            "4",
            "5",
            "6",
            "7",
            "8",
            "9",
            "10",
            "11",
            "12",
            "13",
            "14",
            "15",
            "16",
            "17",
            "18",
            "19",
            "20",
            "21",
            "22",
            "23",
            "24",
          ],
        },
      ],

      yAxis: [
        {
          name:'单位(件)',
          type: "value",
          nameTextStyle:{
            color:'#fff'
          },
          min: 0,
          // max: 140,
          splitNumber: 4,
          splitLine: {
            show: false,
            lineStyle: {
              color: "#00BFF3",
              opacity: 0.23,
            },
          },
          axisLine: {
            show: false,
          },
          axisLabel: {
            show: true,
            margin: 20,
            textStyle: {
              color: "#fff",
            },
          },
          axisTick: {
            show: false,
          },
        },
        {
          type: "value",
          min: 0,
          splitNumber: 4,
          splitLine: {
            show: false,
            lineStyle: {
              color: "#00BFF3",
              opacity: 0.23,
            },
          },
          axisLine: {
            show: false,
          },
          axisLabel: {
            show: true,
            margin: 20,
            textStyle: {
              color: "#fff",
            },
          },
          axisTick: {
            show: false,
          },
        },
      ],
      series: [
        {
          name: "液压异常报警",
          type: "line",
          showAllSymbol: true,
          symbol: "none",
          symbolSize: 10,
          lineStyle: {
            normal: {
              color: "#A582EA",
            },
          },
          label: {
            show: true,
            position: "top",
            textStyle: {
              color: "#A582EA",
            },
          },
          itemStyle: {
            color: "#fff",
            borderColor: "#A582EA",
            borderWidth: 2,
          },
          areaStyle: {
            normal: {
              color: new echarts.graphic.LinearGradient(
                0,
                0,
                0,
                1,
                [
                  {
                    offset: 0,
                    color: "rgba(43,193,145,0.3)",
                  },
                  {
                    offset: 1,
                    color: "rgba(43,193,145,0)",
                  },
                ],
                false
              ),
            },
          },
          data: [
            4,
            7,
            5,
            4,
            3,
            5,
            4,
            7,
            5,
            4,
            3,
            5,
            4,
            7,
            5,
            4,
            3,
            5,
            4,
            7,
            5,
            4,
            3,
            5,
          ], //data.values
        },
        {
          backgroundColor: "rgba(36, 53, 135, 0.298039215686275)",
          name: "费用金额",
          type: "line",
          smooth: true,
          stack: "使用情况",
          symbolSize: "5",
          data: [
            2,
            3,
            4,
            5,
            6,
            10,
            12,
            14,
            16,
            18,
            22,
            24,
            22,
            16,
            14,
            13,
            12,
            11,
            7,
            4,
            6,
            8,
            9,
            14,
          ],
          itemStyle: {
            normal: { color: "rgba(52,177,95,0.9)" },
          },
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
.top,
.top #channel-right-top {
  width: 910px;
  height: 500px;
}

.top .hader {
  position: relative;
  margin-top: 80px;
  margin-left: 42px;
  padding-left: 16px;
  font-size: 30px;
  color: #5cdbe5;
  font-weight: 900;
  line-height: 36px;
}
.top .hader::before {
  position: absolute;
  left: 0;
  width: 1;
  margin-top: 2px;
  height: 30px;
  border: 2px solid #02a5ea;
  content: "";
}
</style>
