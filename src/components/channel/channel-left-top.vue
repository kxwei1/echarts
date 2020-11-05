<template>
  <div class="top">
    <div class="hader">渠道分布</div>
    <div id="channel-left-top"></div>
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
    var myChart = echarts.init(document.getElementById("channel-left-top"));
    var option = {
      title: {
        x: "center",
      },
      // backgroundColor: "#fff",
      tooltip: {
        trigger: "item",
      },
      xAxis: [
        {
          data: ["入职", "离职", "培训", "入职", "离职"],
          axisTick: {
            show: false,
          },
          axisLine: {
            show: false,
          },
          axisLabel: {
            textStyle: {
              color: "#ffe",
              fontSize: "30",
            },
            margin: 20, //刻度标签与轴线之间的距离。
          },
        },
        {
          data: ["10个", "8个", "6个", "10个", "8个"],
          axisTick: {
            show: false,
          },
          axisLine: {
            show: false,
          },
          axisLabel: {
            textStyle: {
              color: "#fff",
              fontSize: "30",
            },
          },
        },
      ],
      yAxis: {
        splitLine: {
          show: false,
        },
        axisTick: {
          show: false,
        },
        axisLine: {
          show: false,
        },
        axisLabel: {
          show: false,
        },
      },
      series: [
        {
          //三个最低下的圆片
          name: "",
          type: "pictorialBar",
          symbolSize: [50, 30],
          symbolOffset: [0, 18],
          z: 12,
          data: [
            {
              name: "",
              value: "100",
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
              name: "",
              value: "101",
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
              name: "",
              value: "81",
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
              name: "",
              value: "100",
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
              name: "",
              value: "101",
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
          ],
        },

        //下半截柱状图
        {
          name: "2020",
          type: "bar",
          barWidth: 50,
          barGap: "-100%",
          itemStyle: {
            //lenged文本
            color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
              {
                offset: 0,
                color: "rgba(55,255,249,1)",
              },
              {
                offset: 1,
                color: "rgba(0,222,215,0.2)",
              },
            ]),
          },

          data: [
            {
              name: "",
              value: "100",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        //第一节下面
                        offset: 0,
                        color: "rgba(0,255,245,0.5)",
                      },
                      {
                        offset: 1,
                        color: "#43bafe",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "",
              value: "101",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        //第二个柱状图下面
                        offset: 0,
                        color: "rgba(0,255,245,0.5)",
                      },
                      {
                        offset: 1,
                        color: "#43bafe",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "",
              value: "81",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        //第三个柱状图下半截
                        offset: 0,
                        color: "rgba(0,255,245,0.5)",
                      },
                      {
                        offset: 1,
                        color: "#43bafe",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "",
              value: "100",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        //第一节下面
                        offset: 0,
                        color: "rgba(0,255,245,0.5)",
                      },
                      {
                        offset: 1,
                        color: "#43bafe",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "",
              value: "101",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        //第二个柱状图下面
                        offset: 0,
                        color: "rgba(0,255,245,0.5)",
                      },
                      {
                        offset: 1,
                        color: "#43bafe",
                      },
                    ],
                  },
                },
              },
            },
          ],
        },

        {
          // 替代柱状图 默认不显示颜色，是最下方柱图（邮件营销）的value值 - 20
          type: "bar",
          barWidth: 50,
          barGap: "-100%",
          stack: "广告",
          itemStyle: {
            color: "transparent",
          },
          data: [100, 102, 81, 100, 102, 81],
        },

        {
          name: "", //头部
          type: "pictorialBar",
          symbolSize: [50, 30],
          symbolOffset: [0, -20],
          z: 12,
          data: [
            {
              name: "",
              value: "320",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(0,89,168,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(0,162,254,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "283",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(0,89,168,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(0,162,254,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "272",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(0,89,168,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(0,162,254,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "320",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(0,89,168,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(0,162,254,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "283",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(0,89,168,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(0,162,254,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
          ],
        },

        {
          name: "",
          type: "pictorialBar",
          symbolSize: [50, 30],
          symbolOffset: [0, -15],
          z: 12,
          data: [
            {
              name: "",
              value: "103",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(89,211,255,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(23,171,255,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "105",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(89,211,255,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(23,171,255,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "84",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(89,211,255,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(23,171,255,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "103",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(89,211,255,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(23,171,255,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
            {
              name: "",
              value: "105",
              symbolPosition: "end",
              itemStyle: {
                normal: {
                  color: new echarts.graphic.LinearGradient(
                    0,
                    0,
                    0,
                    1,
                    [
                      {
                        offset: 0,
                        color: "rgba(89,211,255,1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(23,171,255,1)",
                      },
                    ],
                    false
                  ),
                },
              },
            },
          ],
        },

        {
          name: "2019",
          type: "bar",
          barWidth: 50,
          barGap: "-100%",
          stack: "广告",
          itemStyle: {
            // barBorderRadius: 20,
            color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
              {
                offset: 1,
                color: "rgba(0,255,100,0.5)",
              },
              {
                offset: 1,
                color: "rgba(0,255,100,0.5)",
              },
            ]),
          },
          //上班截开始
          data: [
            {
              name: "关井数",
              value: "220",
              trueVal: "22",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        offset: 0,
                        color: "rgba(6, 55, 151, 1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(6, 55, 151, 0)",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "开井数",
              value: "182",
              trueVal: "18",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        offset: 0,
                        color: "rgba(6, 55, 151, 1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(6, 55, 151, 0)",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "不在线",
              value: "191",
              trueVal: "19",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        offset: 0,
                        color: "rgba(6, 55, 151, 1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(6, 55, 151, 0)",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "关井数",
              value: "220",
              trueVal: "22",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        offset: 0,
                        color: "rgba(6, 55, 151, 1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(6, 55, 151, 0)",
                      },
                    ],
                  },
                },
              },
            },
            {
              name: "开井数",
              value: "182",
              trueVal: "18",
              itemStyle: {
                normal: {
                  color: {
                    x: 0,
                    y: 0,
                    x2: 0,
                    y2: 1,
                    type: "linear",
                    global: false,
                    colorStops: [
                      {
                        offset: 0,
                        color: "rgba(6, 55, 151, 1)",
                      },
                      {
                        offset: 1,
                        color: "rgba(6, 55, 151, 0)",
                      },
                    ],
                  },
                },
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
.top,
.top #channel-left-top {
  width: 910px;
  height: 426px;
}
.top .hader {
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
  margin-left: 50px;
  height: 30px;
  border: 2px solid #02a5ea;
  content: "";
}
</style>
