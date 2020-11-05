<template>
  <div class="mid">
    <div class="hader">渠道分布</div>
    <div id="channel-left-mid"></div>
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
    var myChart = echarts.init(document.getElementById("channel-left-mid"));
    var option = {
      // backgroundColor: "#0f375f",
      legend: [
        {
          orient: "vertical",
          top: "center",
          right: "5%",
          data: ["rose1", "rose2", "rose3", "rose4", "rose5", "rose6"],
          textStyle: {
            color: "#fff",
            fontSize: 22,
          },
        },
        {
          orient: "vertical",
          top: "center",
          right: "17%",
          data: ["rose7", "rose8", "rose9", "rose10", "rose11", "rose12"],
          textStyle: {
            color: "#fff",
            fontSize: 22,
          },
        },
      ],
      tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)",
      },
      series: [
        {
          name: "半径模式",
          type: "pie",
          radius: ["35%", "80%"],
          startAngle: 125,
          clockwise: false,
          center: ["40%", "50%"],
          roseType: "radius",
          label: {
            show: true,
            normal: {
              formatter: "{d}%",
              position: "outside",
              fontSize: 16,
            },
          },
          labelLine: {
            length: 1,
            length2: 20,
            smooth: true,
          },
          data: [
            {
              value: 1,
              name: "rose1",
              itemStyle: {
                color: "rga(50,123,250,0.7)",
              },
            },
            {
              value: 2,
              name: "rose2",
              itemStyle: {
                color: "rgba(244,201,7,0.7)",
              },
            },
            {
              value: 3,
              name: "rose3",
              itemStyle: {
                color: "rgba(23,216,161,0.7)",
              },
            },
            {
              value: 4,
              name: "rose4",
              itemStyle: {
                color: "rgba(122,60,235,0.7)",
              },
            },
            {
              value: 5,
              name: "rose5",
              itemStyle: {
                color: "rgba(15,197,243,0.7)",
              },
            },
            {
              value: 6,
              name: "rose6",
              itemStyle: {
                color: "rgba(89,45,156,0.7)",
              },
            },
            {
              value: 7,
              name: "rose7",
              itemStyle: {
                color: "rga(50,123,250,0.7)",
              },
            },
            {
              value: 8,
              name: "rose8",
              itemStyle: {
                color: "rgba(244,201,7,0.7)",
              },
            },
            {
              value: 9,
              name: "rose9",
              itemStyle: {
                color: "rgba(23,216,161,0.7)",
              },
            },
            {
              value: 10,
              name: "rose10",
              itemStyle: {
                color: "rgba(122,60,235,0.7)",
              },
            },
            {
              value: 11,
              name: "rose11",
              itemStyle: {
                color: "rgba(15,197,243,0.7)",
              },
            },
            {
              value: 12,
              name: "rose12",
              itemStyle: {
                color: "rgba(89,45,156,0.7)",
              },
            },
          ],
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

<style scoped>
.mid,
.mid #channel-left-mid {
  width: 910px;
  height: 426px;
}
.mid .hader {
  margin-top: 30px;
  margin-left: 42px;
  padding-left: 16px;
  font-size: 30px;
  color: #5cdbe5;
  font-weight: 900;
  line-height: 36px;
}
.mid .hader::before {
  position: absolute;
  left: 0;
  width: 1;
  margin-top: 2px;
  margin-left: 50px;
  height: 30px;
  border: 2px solid #02a5ea;
  content: "";
}
</style>
